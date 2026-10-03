# ApprovedBy

Who approved the account-lane run: the user's explicit yes, or the account's LinkedIn Premium (no monthly search cap, so exact runs directly). Relay which.

## Example Usage

```typescript
import { ApprovedBy } from "bereach/models/operations";

let value: ApprovedBy = "premium";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"user" | "premium" | Unrecognized<string>
```