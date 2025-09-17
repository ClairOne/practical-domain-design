# ⚙️ Service Baseline

## Service: `[ServiceName]`

**Description:** [Plain-English one-liner: what this service does in the domain]  
**Type:** [Command | Search | Hybrid]  
**Data source:** [DB table + model | External API | Mixed]  
**Code location:** `[path/to/Service.php]`

---

## 1. Core Operations

List each public method with signature, short purpose, and quirks:

- `methodName(Signature): ReturnType`  
  [One-liner: what it does, any defaults, edge cases, or special behavior]

Example layout:

- `create(CreateXInput $input): XDTO`  
  Creates a new record. Sets default `status = 'new'`.

- `update(X $entity, UpdateXInput $input): XDTO`  
  Updates only provided fields. Nulls ignored.

- `find(string $id): ?XDTO`  
  Returns DTO if found, null otherwise.

- `delete(X $entity): bool`  
  Soft-deletes entity.

---

## 2. Dependencies

- **Models:** `[App\Models\X]`  
- **DTOs:** `[CreateXInput, UpdateXInput, XDTO]`  
- **Other Services/APIs:** `[list any external APIs or sibling services]`

---

## 3. Business Notes

- **Defaults:** [e.g., status starts as 'new']  
- **Special rules:** [e.g., only soft deletes supported]  
- **Partial updates:** [e.g., ignores null fields]  
- **Error handling:** [e.g., findOrFail throws, API calls return error Result]  

---

👉 **In short:** Summarize the service in 2 sentences: what part of the domain it represents, what its main contract is, and any “gotchas.”
