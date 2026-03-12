# SearchLinkedInPostsTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInPostsTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInPostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 743696,
  daily: {
    current: 118293,
    limit: 770336,
  },
  weekly: {
    current: 124044,
    limit: 695658,
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `code`                                                                                           | [operations.SearchLinkedInPostsCode](../../models/operations/search-linked-in-posts-code.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `message`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `docs`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before retrying.                                                                 |
| `daily`                                                                                          | [operations.SearchLinkedInPostsDaily](../../models/operations/search-linked-in-posts-daily.md)   | :heavy_check_mark:                                                                               | Current and max daily usage (null if no daily cap).                                              |
| `weekly`                                                                                         | [operations.SearchLinkedInPostsWeekly](../../models/operations/search-linked-in-posts-weekly.md) | :heavy_check_mark:                                                                               | Current and max weekly usage (null if no weekly cap).                                            |