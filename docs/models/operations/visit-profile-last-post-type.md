# VisitProfileLastPostType

LinkedIn post type: 'ugcPost' = standard post, 'share' = native share/repost, 'activity' = legacy format.

## Example Usage

```typescript
import { VisitProfileLastPostType } from "bereach/models/operations";

let value: VisitProfileLastPostType = "share";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"activity" | "ugcPost" | "share" | Unrecognized<string>
```