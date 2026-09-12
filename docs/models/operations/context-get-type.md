# ContextGetType

## Example Usage

```typescript
import { ContextGetType } from "bereach/models/operations";

let value: ContextGetType = "system:cache_warning";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"task:completed" | "task:failed" | "reply:received" | "connection:accepted" | "campaign:rate_limited" | "campaign:linkedin_expired" | "credential:llm_error" | "credential:linkedin_long_broken" | "contact:handover" | "drafts:pending" | "system:cache_warning" | Unrecognized<string>
```