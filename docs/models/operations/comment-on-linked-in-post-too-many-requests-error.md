# CommentOnLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { CommentOnLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: CommentOnLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 810244,
  daily: {
    current: 293910,
    limit: 261485,
  },
  weekly: {
    current: 696909,
    limit: 627861,
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `code`                                                                                                | [operations.CommentOnLinkedInPostCode](../../models/operations/comment-on-linked-in-post-code.md)     | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `message`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `docs`                                                                                                | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `retryAfter`                                                                                          | *number*                                                                                              | :heavy_check_mark:                                                                                    | Seconds to wait before retrying.                                                                      |
| `daily`                                                                                               | [operations.CommentOnLinkedInPostDaily](../../models/operations/comment-on-linked-in-post-daily.md)   | :heavy_check_mark:                                                                                    | Current and max daily usage (null if no daily cap).                                                   |
| `weekly`                                                                                              | [operations.CommentOnLinkedInPostWeekly](../../models/operations/comment-on-linked-in-post-weekly.md) | :heavy_check_mark:                                                                                    | Current and max weekly usage (null if no weekly cap).                                                 |