# ProfileVisitDaily

Daily usage counter (resets at midnight UTC)

## Example Usage

```typescript
import { ProfileVisitDaily } from "bereach/models/operations";

let value: ProfileVisitDaily = {
  current: 405285,
  limit: 126126,
  remaining: 290664,
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `current`                                                        | *number*                                                         | :heavy_check_mark:                                               | Number of actions used in this window                            |
| `limit`                                                          | *number*                                                         | :heavy_check_mark:                                               | Maximum allowed actions in this window (with multiplier applied) |
| `remaining`                                                      | *number*                                                         | :heavy_check_mark:                                               | Actions remaining before hitting the limit                       |