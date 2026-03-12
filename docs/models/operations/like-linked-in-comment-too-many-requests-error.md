# LikeLinkedInCommentTooManyRequestsError

## Example Usage

```typescript
import { LikeLinkedInCommentTooManyRequestsError } from "bereach/models/operations";

let value: LikeLinkedInCommentTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 248293,
  daily: {
    current: 272520,
    limit: 141743,
  },
  weekly: {
    current: 502902,
    limit: 208664,
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `code`                                                                                           | [operations.LikeLinkedInCommentCode](../../models/operations/like-linked-in-comment-code.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `message`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `docs`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before retrying.                                                                 |
| `daily`                                                                                          | [operations.LikeLinkedInCommentDaily](../../models/operations/like-linked-in-comment-daily.md)   | :heavy_check_mark:                                                                               | Current and max daily usage (null if no daily cap).                                              |
| `weekly`                                                                                         | [operations.LikeLinkedInCommentWeekly](../../models/operations/like-linked-in-comment-weekly.md) | :heavy_check_mark:                                                                               | Current and max weekly usage (null if no weekly cap).                                            |