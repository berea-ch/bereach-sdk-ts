# GetProfileType

LinkedIn post type: 'ugcPost' = standard post, 'share' = native share/repost, 'activity' = legacy format.

## Example Usage

```typescript
import { GetProfileType } from "bereach/models/operations";

let value: GetProfileType = "activity";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"activity" | "ugcPost" | "share" | Unrecognized<string>
```