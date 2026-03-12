# EditLinkedInCommentTooManyRequestsError

## Example Usage

```typescript
import { EditLinkedInCommentTooManyRequestsError } from "bereach/models/operations";

let value: EditLinkedInCommentTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 417673,
  daily: null,
  weekly: {
    current: 608522,
    limit: 598739,
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `code`                                                                                           | [operations.EditLinkedInCommentCode](../../models/operations/edit-linked-in-comment-code.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `message`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `docs`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before retrying.                                                                 |
| `daily`                                                                                          | [operations.EditLinkedInCommentDaily](../../models/operations/edit-linked-in-comment-daily.md)   | :heavy_check_mark:                                                                               | Current and max daily usage (null if no daily cap).                                              |
| `weekly`                                                                                         | [operations.EditLinkedInCommentWeekly](../../models/operations/edit-linked-in-comment-weekly.md) | :heavy_check_mark:                                                                               | Current and max weekly usage (null if no weekly cap).                                            |