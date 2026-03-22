# CollectLikesTooManyRequestsError

## Example Usage

```typescript
import { CollectLikesTooManyRequestsError } from "bereach/models/operations";

let value: CollectLikesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 311843,
  daily: {
    current: 33179,
    limit: 839384,
  },
  weekly: {
    current: 300107,
    limit: 385944,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `code`                                                                           | [operations.CollectLikesCode](../../models/operations/collect-likes-code.md)     | :heavy_check_mark:                                                               | N/A                                                                              |
| `message`                                                                        | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `docs`                                                                           | *string*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |
| `retryAfter`                                                                     | *number*                                                                         | :heavy_check_mark:                                                               | Seconds to wait before retrying.                                                 |
| `daily`                                                                          | [operations.CollectLikesDaily](../../models/operations/collect-likes-daily.md)   | :heavy_check_mark:                                                               | Current and max daily usage (null if no daily cap).                              |
| `weekly`                                                                         | [operations.CollectLikesWeekly](../../models/operations/collect-likes-weekly.md) | :heavy_check_mark:                                                               | Current and max weekly usage (null if no weekly cap).                            |