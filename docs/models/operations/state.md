# State

What the account is doing: nothing_queued means nobody is waiting, sending means invitations are going out, spacing means it is between two invitations, blocked means nothing is going out.

## Example Usage

```typescript
import { State } from "bereach/models/operations";

let value: State = "nothing_queued";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"nothing_queued" | "sending" | "spacing" | "blocked" | Unrecognized<string>
```