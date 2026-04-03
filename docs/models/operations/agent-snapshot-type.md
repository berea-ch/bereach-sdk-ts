# AgentSnapshotType

## Example Usage

```typescript
import { AgentSnapshotType } from "bereach/models/operations";

let value: AgentSnapshotType = "campaign:target_reached";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"task:completed" | "task:failed" | "reply:received" | "connection:accepted" | "campaign:target_reached" | "campaign:completed" | "campaign:paused" | Unrecognized<string>
```