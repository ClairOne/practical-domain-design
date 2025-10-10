# Part 3 - Tactical Feedback Loop

## Tech Stack & Coding Standards

---

## 1. Stack Overview

* **Framework:** Laravel 12
* **Auth:** Passport (scopes for web-access, api-access, plus jobs/commands where appropriate)
* **Authorization:** Spatie Permission + Laravel Gates/Policies
* **UI:** Volt + Flux
* **DB:** MySQL 8.x
* **Testing:** PEST
* **Transport:** UI routes, API routes, Jobs, Commands
* **Config:** `.env` flags to enable/disable modules

👉 **In short:** Everything hangs off Laravel conventions. Keep it boring, predictable, and testable.

---

## 2. Module Conventions

* **Strategic mapping:** Each Department → one Module namespace (Domain and Module are interchangeable).
* **Namespace:** `App/<Module>` for Actions, Services, DTOs, and optionally Models; or `App/Models` for global models when appropriate.
* **Enablement:** Each module has an `.env` toggle `MODULE_<NAME>=true|false` and a module service provider to register routes and bindings.
* **Seams:** Modules should not reach into each other’s internals. Cross-module communication goes through Services or Events.

### Folder skeleton

```
app/<Module>/
  Actions/
  Services/
  DTO/
  Policies/
  Providers/
  Routes/
    web.php
    api.php
  Jobs/
  Commands/
  Exceptions/
  Support/  # helpers specific to module
  Listeners/
```

---

## 3. Routing

* **Split by module:** Each module owns `Routes/web.php` and `Routes/api.php` registered by its provider.
* **Volt first:** Favor Volt based routes for UI. Controllers remain for non-Volt endpoints or when composition is clearer.
* **Thin edges:** Route → FormRequest → Action. Volt functions and controllers stay thin and delegate immediately to Actions.
* **Passport scopes:** Apply `web-access` or `api-access` at the route middleware layer.

---

## 4. Entry Points

* **Allowed:** UI Routes, API Routes, Jobs, Commands, Listeners.
* **Rule:** All entry points call an **Action**. No direct Service calls from transport edges or listeners.
* **Background work:** Jobs wrap Actions. Commands are thin facades over Actions for ops workflows. Listeners also delegate directly to Actions and contain no logic.

---

## 5. Actions

* **Role:** Tactical mirror of a Strategic Workflow. Orchestrates Services and emits Events.
* **Contract:** Accepts an `ActionInputDTO`, returns an `OutputDTO` or ViewModel.
* **Validation:** Inputs validated by FormRequest or explicit DTO validators.
* **Authorization:** Verify Spatie Permissions before invoking Services or emitting Events.
* **Side effects:** Only through Services. No direct DB writes here.

---

## 6. Services

* **Role:** Tactical mirror of a Strategic Operation. Encapsulates business logic.
* **Authorization:** Enforce Gates/Policies inside Services before mutating anything.
* **I/O contracts:** `ServiceInputDTO` and `ServiceOutputDTO`. Never return Eloquent models to callers outside the service.
* **Cross-module:** Allowed via service interfaces. Bind interfaces in module provider.

---

## 7. Models

* **Scope:** Models may be global in `App/Models` or module scoped in `App/<Module>/Models` when boundaries are strong.
* **Keep thin:** No business rules beyond relationships, casts, scopes, and accessors where unavoidable.
* **Policies:** Define access rules here, enforced consistently by Services.

---

## 8. DTOs

* **Why:** Deterministic contracts between layers. Simplifies testing with PEST.
* **Types:** `ActionInputDTO`, `ResultDTO/OutputDTO`, `ServiceInputDTO`, `ServiceOutputDTO`, plus View DTOs for UI.
* **Rules:** Immutable where practical. No framework coupling inside DTOs.

---

## 9. Validation

* **FormRequest:** Mandatory at transport edges for incoming data.
* **Service-level checks:** Business rule validation lives in Services, not controllers.

---

## 10. Authorization

* **Order of checks:**

  1. Passport scope at route (entry gate)
  2. Spatie Permission for capability checks
  3. Gate for contextual rules
  4. Policy for record-level decisions
* **Placement:** Services own the enforcement before performing mutations.

---

## 11. Environment Flags

* **Module toggles:** `.env` variables enable or disable module route registration and scheduled jobs.
* **Feature flags:** Use config or a simple toggle service for sub-module features. Keep flags discoverable and test-covered.

---

## 12. Testing

* **PEST:** Required for units, services, and actions.
* **DTO tests:** Verify serialization and invariants.
* **Policy tests:** Cover critical access paths and denial cases.
* **Action tests:** Treat as integration at the module seam.
* **Event/Listener tests:** Ensure events are emitted correctly and listeners properly dispatch Actions.

---

## 13. Database

* **Migrations:** Live alongside the module or in central `database/migrations` with clear naming: `<timestamp>_<module>_<table>_...`.
* **Seeds:** Module-specific seeders where useful. Keep idempotent.
* **Constraints:** Default to constraint logic in Services for situational data integrity. DB-level constraints may be used sparingly, but Services are the source of truth and surface friendly errors.

---

## 14. Error Handling

* **Exceptions:** Module-specific exceptions under `Exceptions/`. Bubble to a standard handler with problem details.
* **Error boundaries:** Catch at Action edges, convert to domain-safe responses or problem detail objects.
* **User messaging:** Services surface friendly errors - no raw framework exceptions should leak to UI or API clients.

---

## 15. Events

* **Emit:** Use Laravel Events from Actions or Services to represent meaningful business facts.
* **Listeners:** **Must only invoke Actions** and contain no business logic. Keep them single-purpose and idempotent.
* **Conventions:**

  * Events named in past tense, e.g., `TeamCreated`, `InvoiceSent`.
  * Listeners live under `Listeners/` within the module and only dispatch Actions (no direct Service or DB calls).

---

## 16. Observability

* **Structured logging:** Prefer JSON logs for aggregation. Always include correlation IDs (`request_id`, `action_run_id`).
* **Metrics:** Count key events and failures per module/action. Naming convention: `<module>.<action>.<result>`.
* **Performance timing:** Log execution time of hot path Services/Actions for insight.
* **Event trails:** Log event emissions and listener outcomes to form an audit trail.

---

## 17. Naming & Style

* **Actions:** VerbNoun, e.g., `ManageTeam`, `IssueRefund`.
* **Services:** `<Noun>Service` with verb methods, e.g., `TeamService.addCoach()`.
* **DTOs:** Suffix with DTO, e.g., `CreateTeamInputDTO`.
* **Routes:** Grouped by module prefix. No long anonymous closures except Volt pages.

---

## 18. Dependencies & Boundaries

* **No hidden reach-ins:** A module cannot use another module’s internal classes directly.
* **Interfaces:** Cross-module use only via interfaces bound in providers.
* **Events as seams:** Prefer events for low coupling.

---

## 19. Tactical Artifacts Mapping

* **Module Detail:** Maps to Department Detail
* **Action Detail:** Maps to Workflow Detail
* **Service Detail:** Maps to Operation Step Detail
* **Model Detail:** Maps to Business Entity Detail

---

👉 **In short:** Keep edges thin, center logic in Services, orchestrate with Actions, guard with Policies, and move data in DTOs. Boring code today beats clever bugs tomorrow.
