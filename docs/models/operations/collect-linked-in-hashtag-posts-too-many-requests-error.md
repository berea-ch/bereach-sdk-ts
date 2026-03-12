# CollectLinkedInHashtagPostsTooManyRequestsError

## Example Usage

```typescript
import { CollectLinkedInHashtagPostsTooManyRequestsError } from "bereach/models/operations";

let value: CollectLinkedInHashtagPostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 703694,
  daily: {
    current: 808873,
    limit: 873229,
  },
  weekly: {
    current: 699391,
    limit: 886031,
  },
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                            | [operations.CollectLinkedInHashtagPostsCode](../../models/operations/collect-linked-in-hashtag-posts-code.md)     | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `message`                                                                                                         | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `docs`                                                                                                            | *string*                                                                                                          | :heavy_minus_sign:                                                                                                | N/A                                                                                                               |
| `retryAfter`                                                                                                      | *number*                                                                                                          | :heavy_check_mark:                                                                                                | Seconds to wait before retrying.                                                                                  |
| `daily`                                                                                                           | [operations.CollectLinkedInHashtagPostsDaily](../../models/operations/collect-linked-in-hashtag-posts-daily.md)   | :heavy_check_mark:                                                                                                | Current and max daily usage (null if no daily cap).                                                               |
| `weekly`                                                                                                          | [operations.CollectLinkedInHashtagPostsWeekly](../../models/operations/collect-linked-in-hashtag-posts-weekly.md) | :heavy_check_mark:                                                                                                | Current and max weekly usage (null if no weekly cap).                                                             |