# PendingConnection

Connection request status: 'pending' if request was sent successfully, 'failed' if request failed today, 'none' if not tracked

## Example Usage

```typescript
import { PendingConnection } from "bereach/models/operations";

let value: PendingConnection = "pending";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "failed" | "none" | Unrecognized<string>
```