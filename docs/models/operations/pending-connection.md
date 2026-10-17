# PendingConnection

'pending' when an invitation to this person went out in the last 7 days, otherwise 'none'. Somebody still waiting in line reads 'none': ask for the connection status. A repeat visit within a day repeats the first answer.

## Example Usage

```typescript
import { PendingConnection } from "bereach/models/operations";

let value: PendingConnection = "pending";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "none" | Unrecognized<string>
```