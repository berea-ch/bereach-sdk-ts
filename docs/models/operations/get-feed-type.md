# GetFeedType

LinkedIn post type: 'ugcPost' = standard post, 'share' = native share/repost, 'activity' = legacy format.

## Example Usage

```typescript
import { GetFeedType } from "bereach/models/operations";

let value: GetFeedType = "share";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"activity" | "ugcPost" | "share" | Unrecognized<string>
```