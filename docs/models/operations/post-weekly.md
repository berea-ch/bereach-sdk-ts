# PostWeekly

Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.

## Example Usage

```typescript
import { PostWeekly } from "bereach/models/operations";

let value: PostWeekly = {
  current: 736610,
  limit: 881513,
  remaining: 767797,
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `current`                                                        | *number*                                                         | :heavy_check_mark:                                               | Number of actions used in this window                            |
| `limit`                                                          | *number*                                                         | :heavy_check_mark:                                               | Maximum allowed actions in this window (with multiplier applied) |
| `remaining`                                                      | *number*                                                         | :heavy_check_mark:                                               | Actions remaining before hitting the limit                       |