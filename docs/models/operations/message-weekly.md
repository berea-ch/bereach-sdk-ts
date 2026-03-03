# MessageWeekly

Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.

## Example Usage

```typescript
import { MessageWeekly } from "bereach/models/operations";

let value: MessageWeekly = {
  current: 188187,
  limit: 665961,
  remaining: 248087,
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `current`                                                        | *number*                                                         | :heavy_check_mark:                                               | Number of actions used in this window                            |
| `limit`                                                          | *number*                                                         | :heavy_check_mark:                                               | Maximum allowed actions in this window (with multiplier applied) |
| `remaining`                                                      | *number*                                                         | :heavy_check_mark:                                               | Actions remaining before hitting the limit                       |