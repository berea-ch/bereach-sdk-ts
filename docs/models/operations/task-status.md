# TaskStatus

## Example Usage

```typescript
import { TaskStatus } from "bereach/models/operations";

let value: TaskStatus = "accepted";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"queued" | "dispatched" | "accepted" | "running" | "succeeded" | "failed" | "cancelled" | Unrecognized<string>
```