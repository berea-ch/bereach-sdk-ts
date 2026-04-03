# EventsFeedType

## Example Usage

```typescript
import { EventsFeedType } from "bereach/models/operations";

let value: EventsFeedType = "campaign:paused";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"task:completed" | "task:failed" | "reply:received" | "connection:accepted" | "campaign:target_reached" | "campaign:completed" | "campaign:paused" | Unrecognized<string>
```