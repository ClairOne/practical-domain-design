# 🧠 Tactical Mud Map - Brain Dump

> Dump what you can see in the codebase.  
> Duplicates and blanks are fine.  
> If there’s no service class, write the behavior as a **pseudo-service**.  
> We’ll organize later into Modules → Actions → Services → Models.

| Entry Point (Route/Job/Command) | Action Name (Observed Sequence) | Operation Snippets | Service or Pseudo-service | Model(s) Touched | Notes |
|---------------------------------|---------------------------------|--------------------|---------------------------|------------------|-------|
| `PUT /teams/{id}` → `TeamController@update` | Update Team | validate input, update name, fire event | TeamService.updateName() or **[inline]** name update | Team | Permissions live in controller, not policy |
| `POST /invites` → `InviteController@create` | Create Invite | build invite, send email, audit log | InviteService.send() | Invite, Team, User | Email via raw `Mail::to()` in controller |
| `artisan orders:process` | Process Orders | load due orders, calc totals, mark paid | **[pseudo]** OrderProcessing | Order, Payment | Heavy branching - retries hidden in loop |
|                                 |                                 |                    |                           |                  |       |
|                                 |                                 |                    |                           |                  |       |