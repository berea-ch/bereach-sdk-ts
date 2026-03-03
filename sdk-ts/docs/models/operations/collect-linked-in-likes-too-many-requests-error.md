# CollectLinkedInLikesTooManyRequestsError

## Example Usage

```typescript
import { CollectLinkedInLikesTooManyRequestsError } from "bereach/models/operations";

let value: CollectLinkedInLikesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 910433,
  daily: {
    current: 504727,
    limit: 873070,
  },
  weekly: {
    current: 37088,
    limit: 774257,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.CollectLinkedInLikesCode](../../models/operations/collect-linked-in-likes-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.CollectLinkedInLikesDaily](../../models/operations/collect-linked-in-likes-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.CollectLinkedInLikesWeekly](../../models/operations/collect-linked-in-likes-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |