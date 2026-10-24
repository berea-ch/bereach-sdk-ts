# FindEmailsStatus

found: found now, one email credit. already_saved: the email was already on the contact, free. already_found: found earlier for this person, who is not saved, free. not_found: none found, free. not_looked_up: no email credit left, free. unavailable: could not be looked up now, free. unknown_contact: no saved person has this contact id, free.

## Example Usage

```typescript
import { FindEmailsStatus } from "bereach/models/operations";

let value: FindEmailsStatus = "already_saved";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"found" | "already_saved" | "already_found" | "not_found" | "not_looked_up" | "unavailable" | "unknown_contact" | Unrecognized<string>
```