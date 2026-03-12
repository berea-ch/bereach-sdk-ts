# UnlikeLinkedInCommentTooManyRequestsError

## Example Usage

```typescript
import { UnlikeLinkedInCommentTooManyRequestsError } from "bereach/models/operations";

let value: UnlikeLinkedInCommentTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 673303,
  daily: {
    current: 917626,
    limit: 670789,
  },
  weekly: {
    current: 561989,
    limit: 915842,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `code`                                                                                               | [operations.UnlikeLinkedInCommentCode](../../models/operations/unlike-linked-in-comment-code.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `message`                                                                                            | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `docs`                                                                                               | *string*                                                                                             | :heavy_minus_sign:                                                                                   | N/A                                                                                                  |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before retrying.                                                                     |
| `daily`                                                                                              | [operations.UnlikeLinkedInCommentDaily](../../models/operations/unlike-linked-in-comment-daily.md)   | :heavy_check_mark:                                                                                   | Current and max daily usage (null if no daily cap).                                                  |
| `weekly`                                                                                             | [operations.UnlikeLinkedInCommentWeekly](../../models/operations/unlike-linked-in-comment-weekly.md) | :heavy_check_mark:                                                                                   | Current and max weekly usage (null if no weekly cap).                                                |