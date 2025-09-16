# 📦 Module Detail

---

## ℹ️ Info
**Name:**  
[Module or slice name - e.g., Teams]

**Description:**  
[What this slice of code actually does]

**Primary Contact:**  
- Name: [Full Name]  
- Email: [Email]  
- Phone: [Phone]

---

## ⚡ Actions (Entry Points)

> Entry points that kick off business work. When in doubt, list controller methods, jobs, commands.

| # | Entry Point | Action Name | Description | Trigger / Source | Owner |
|---|---|---|---|---|---|
| 1 | TeamController@update | Update Team | Update team metadata | HTTP UI | [Name] |
| 2 | InviteController@create | Create Invite | Create and email invite | API | [Name] |

---

## 🛠️ Services and Pseudo-services

> Real services or named chunks of repeated data-access behavior. If it isn’t a class, label it **[pseudo]** and describe where it lives.

| # | Service or Pseudo | Where it lives | What it does | Notes |
|---|---|---|---|---|
| 1 | TeamService.updateName() | `App/Services/TeamService.php` | Mutates `Team.name` | Skips Policy check |
| 2 | **[pseudo]** OrderProcessing | scattered in `OrderJob@process` | Loads due orders, retries | Hidden backoff logic |

---

## 🧩 Models

| # | Model | Reads | Writes | Typical filters | Notes |
|---|---|---|---|---|---|
| 1 | Team | TeamController@edit | TeamController@update | `org_id = X` | Business rules live in model |
| 2 | Invite | InviteController@index | InviteController@create | `team_id = X` | Email send coupled to save |

---

## 🗂️ Version
- **Created:** [Date]  
- **Last Updated:** [Date]  
- **History:** [Changes]  
