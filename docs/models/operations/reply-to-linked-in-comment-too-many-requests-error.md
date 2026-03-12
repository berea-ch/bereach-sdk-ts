# ReplyToLinkedInCommentTooManyRequestsError

## Example Usage

```typescript
import { ReplyToLinkedInCommentTooManyRequestsError } from "bereach/models/operations";

let value: ReplyToLinkedInCommentTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 56836,
  daily: {
    current: 204093,
    limit: 780151,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                  | [operations.ReplyToLinkedInCommentCode](../../models/operations/reply-to-linked-in-comment-code.md)     | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `message`                                                                                               | *string*                                                                                                | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `docs`                                                                                                  | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `retryAfter`                                                                                            | *number*                                                                                                | :heavy_check_mark:                                                                                      | Seconds to wait before retrying.                                                                        |
| `daily`                                                                                                 | [operations.ReplyToLinkedInCommentDaily](../../models/operations/reply-to-linked-in-comment-daily.md)   | :heavy_check_mark:                                                                                      | Current and max daily usage (null if no daily cap).                                                     |
| `weekly`                                                                                                | [operations.ReplyToLinkedInCommentWeekly](../../models/operations/reply-to-linked-in-comment-weekly.md) | :heavy_check_mark:                                                                                      | Current and max weekly usage (null if no weekly cap).                                                   |