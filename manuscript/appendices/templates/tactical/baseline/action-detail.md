# ⚡ Action Detail

---

## ℹ️ Info
**Name:**  
[Action name - e.g., Update Team]

**Entry Point:**  
[Route/controller, job, command]

**Description:**  
[Plain-English what it achieves]

**Primary Contact:**  
- Name / Email / Phone

---

## 🛠️ Flow (Step-by-step)

> Each step is an operation or call you can point at. Use **[inline]** when the logic isn’t in a service.

| # | Step | Where | Services/Models | Notes / Conditions |
|---|---|---|---|---|
| 1 | validate request | controller | - | Missing form request |
| 2 | check permission | **[inline]** controller | User, Team | Should be Policy |
| 3 | update name | TeamService.updateName() or **[inline]** | Team | No audit trail |
| 4 | dispatch event | **[inline]** | TeamUpdated | Downstream email |

---

## 🧩 Data touchpoints

- Reads: [models and fields]  
- Writes: [models and fields]  
- Side effects: [emails, jobs, events]

---

## 🗒️ Risks
- [Tight coupling, global state, silent catches, etc.]

---

## 🗂️ Version
- Created / Updated / History