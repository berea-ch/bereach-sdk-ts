# CollectLinkedInPostsTooManyRequestsError

## Example Usage

```typescript
import { CollectLinkedInPostsTooManyRequestsError } from "bereach/models/operations";

let value: CollectLinkedInPostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 241138,
  daily: {
    current: 360612,
    limit: 319639,
  },
  weekly: {
    current: 932609,
    limit: 44202,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.CollectLinkedInPostsCode](../../models/operations/collect-linked-in-posts-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.CollectLinkedInPostsDaily](../../models/operations/collect-linked-in-posts-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.CollectLinkedInPostsWeekly](../../models/operations/collect-linked-in-posts-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |