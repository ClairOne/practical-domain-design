# Practical Domain Design - Complete Manuscript
**Generated:** Sat Sep 20 02:18:48 PM EST 2025
**Repository:** https://github.com/ClairOne/practical-domain-design

> This file is auto-generated for review purposes. 
> Direct link for AI analysis: https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/BOOK_REVIEW.md

---

## Table of Contents

## Manuscript Stats
- **Total Chapters:** 1
- **Total Words:** 0
- **Total TODOs:** 0
- **Raw GitHub URLs:** All chapters available at `https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/manuscript/chapters/`

---

## 📖 06.2.0.strategic-loop.md


---

## 📖 08.1.strategic-to-tactical-translation-map.md

# 8.1 Strategic to Tactical Translation Map



| Strategic term            | Tactical - Laravel    | Notes                                                                                                                                                     |
| ------------------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Department                | Domain                | Top-level business area and code namespace. Example: `App/Domain/PainPoints`.                                                                             |
| Workflow                  | Action                | Multi-step SOP composed of Operations. Implemented as one coordinating Action that may call other Actions.                                                |
| Operation                 | Service.function      | Single-step unit of business work. E.g. Team.update                                                                                                       |
| Business Entity           | Model                 | The noun of the system. Keep models thin.                                                                                                                 |
| Workflow Request          | ActionInputDTO        | Input to a coordinating Action. Includes step list, dependencies, and handoff expectations.                                                               |
| Workflow Response         | ResultDTO / OutputDTO | Composite business response with run id, final status, and next step hints.                                                                               |
| Operation Request         | ServiceInputDTO       | Input contract for a Service. For Search use criteria DTOs; for Change use command DTOs.                                                                  |
| Operation Response        | ServiceOutputDTO      | Output contract from a Service. Returns entity/view DTOs or paginated sets - never Eloquent models.                                                       |
| Business Input Form       | FormRequest           | Transport-layer validation. Converts to ActionInputDTO.                                                                                                   |
| Access Channel            | Passport Scope        | Broad transport gate - web, api, job, command. Checked at entry. After entry, Permissions + Gates + Policies govern capabilities and records.             |
| Permission                | Spatie Permission     | Named capability entity - role or grant based. No specific record context. Used for UI show/hide and quick guards.                                        |
| Role                      | Spatie Group          | Business role mapped to a Spatie Group that aggregates Permissions for assignment to users.                                                               |
| Access Rule               | Gate                  | Contextual rule at workflow boundaries: combine permissions with runtime context like business hours, feature flags, maintenance mode. Can call Policies. |
| Access Policy             | Policy                | Per-entity decision: ownership, record state, org constraints for a specific instance.                                                                    |
| Business Event            | Event                 | Past-tense fact like `PainPointCreated`. Emitted by Services or Actions.                                                                                  |
| Business Event Subscriber | Listener              | Handles side effects of Business Signals. Single classification - tactical attributes defined later.                                                      |
| Notification              | Notification          | Messages to humans or channels triggered by Events/Actions.                                                                                               |

### Access control - order of checks

1. **Access Channel - Passport Scope**: can this token enter via web, api, job, or command
2. **Permission - Spatie Permission**: named capability like `team.create`, `team.update`
3. **Access Rule - Gate**: context checks - business hours, feature flags, maintenance
4. **Access Policy - Policy**: record-level rules - ownership, role on team, attribute limits

- Principle: the deeper you go, the more restrictive. Trust at higher layers - verify at lower layers. Lower layers should not depend on the entry channel.

---

## 📖 0.chapter-layout.md

Here’s a clean, funnel-style outline for the **Strategic Domain Design** chapter. Each section builds on the last like steps in a sales journey - you start with “why should I care?” and end with “here’s how we live with it long-term.” I’ve also added what you lose if you cut a section.

---

# 📘 Strategic Domain Design - Chapter Outline

### Section 1: Introduction / Overview

**Value:** Sets the stage. Explains what Strategic Domain Design even is, why it matters, and promises the reader “this won’t be another dry theory dump.”
**If skipped:** Readers won’t know what they’re signing up for or why they should keep turning pages. They’ll bounce.

---

### Section 2: The Problem We’re Trying to Solve

**Value:** Paints the pain in vivid color - translation fatigue, Agile Theater, midnight releases. Helps the reader say, “yep, that’s us.”
**If skipped:** PDD looks like a random new framework instead of a cure for their real headaches.

---

### Section 3: How PDD Solves It

**Value:** Introduces PDD as the antidote. High-level principles, not yet the gritty details. Think promises, not processes.
**If skipped:** PDD feels like a hammer in search of a nail. Readers won’t connect it to their problems.

---

### Section 4: Getting Started With a Baseline

**Value:** Explains the “day 1 snapshot.” Baseline docs and why we freeze the mess before fixing it. Gives small teams a low-cost on-ramp.
**If skipped:** Teams dive straight into process changes without a map of where they started. Harder to measure improvement and avoid chaos.

---

### Section 5: Begin the Loop

**Value:** The beating heart of PDD - short, feedback-driven cycles. Shows how teams actually move from baseline to better.
**If skipped:** PDD devolves into another static design doc exercise instead of a living system. Readers never see how learning drives design.

---

### Section 6: Making It Canon

**Value:** Explains how lessons from the loop get promoted into the new “source of truth.” Prevents endless churn.
**If skipped:** Teams either get stuck in permanent loop mode (never stabilizing) or lock in bad decisions too early.

---

### Section 7: Living With It (Scaling, Drift, and Renewal)

**Value:** Helps teams understand what happens after adoption - how to keep the canon fresh, deal with team growth, or reboot the baseline if things drift.
**If skipped:** PDD looks like a one-and-done playbook, not a sustainable practice. Readers won’t know how to adapt when reality changes.

---

👉 In short: the outline flows like a customer journey -

* **Why care** (Intro + Problem)
* **Why this works** (PDD Solution)
* **How to start** (Baseline)
* **How to improve** (Loop)
* **How to lock in** (Canon)
* **How to sustain** (Living With It)

---

Do you want me to **expand each section into 2-3 sample paragraphs** in book voice so you can see how the flow actually reads, or keep it at this outline level for now?

---

