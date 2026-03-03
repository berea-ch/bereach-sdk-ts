# PendingConnection

Connection request status: 'pending' if request was sent successfully, 'failed' if request failed today, 'none' if not tracked

## Example Usage

```typescript
import { PendingConnection } from "bereach/models/operations";

let value: PendingConnection = "pending";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"pending" | "failed" | "none" | Unrecognized<string>
```