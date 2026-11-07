# FindPhonesStatus

found: found now, charged. already_saved: the number was already on the contact, free. already_found: found earlier for this person, free. not_found: none found, free. not_looked_up: not enough left to spend, free. unavailable: could not be looked up now, free. unknown_contact: no saved person has this contact id, free.

## Example Usage

```typescript
import { FindPhonesStatus } from "bereach/models/operations";

let value: FindPhonesStatus = "not_looked_up";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"found" | "already_saved" | "already_found" | "not_found" | "not_looked_up" | "unavailable" | "unknown_contact" | Unrecognized<string>
```