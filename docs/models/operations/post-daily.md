# PostDaily

Daily usage counter (resets at midnight UTC). Null if not configured for this action type.

## Example Usage

```typescript
import { PostDaily } from "bereach/models/operations";

let value: PostDaily = {
  current: 312726,
  limit: 5053,
  remaining: 239367,
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `current`                                                        | *number*                                                         | :heavy_check_mark:                                               | Number of actions used in this window                            |
| `limit`                                                          | *number*                                                         | :heavy_check_mark:                                               | Maximum allowed actions in this window (with multiplier applied) |
| `remaining`                                                      | *number*                                                         | :heavy_check_mark:                                               | Actions remaining before hitting the limit                       |