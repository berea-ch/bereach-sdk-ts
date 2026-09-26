# EventsFeedType

## Example Usage

```typescript
import { EventsFeedType } from "bereach/models/operations";

let value: EventsFeedType = "system:cache_warning";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"task:completed" | "task:failed" | "reply:received" | "connection:accepted" | "campaign:rate_limited" | "campaign:linkedin_expired" | "credential:llm_error" | "credential:linkedin_long_broken" | "contact:handover" | "drafts:pending" | "system:cache_warning" | Unrecognized<string>
```