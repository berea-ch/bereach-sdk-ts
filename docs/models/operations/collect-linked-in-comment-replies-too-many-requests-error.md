# CollectLinkedInCommentRepliesTooManyRequestsError

## Example Usage

```typescript
import { CollectLinkedInCommentRepliesTooManyRequestsError } from "bereach/models/operations";

let value: CollectLinkedInCommentRepliesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 877228,
  daily: {
    current: 101400,
    limit: 597560,
  },
  weekly: {
    current: 435825,
    limit: 141097,
  },
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                                | [operations.CollectLinkedInCommentRepliesCode](../../models/operations/collect-linked-in-comment-replies-code.md)     | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `message`                                                                                                             | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `docs`                                                                                                                | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | N/A                                                                                                                   |
| `retryAfter`                                                                                                          | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | Seconds to wait before retrying.                                                                                      |
| `daily`                                                                                                               | [operations.CollectLinkedInCommentRepliesDaily](../../models/operations/collect-linked-in-comment-replies-daily.md)   | :heavy_check_mark:                                                                                                    | Current and max daily usage (null if no daily cap).                                                                   |
| `weekly`                                                                                                              | [operations.CollectLinkedInCommentRepliesWeekly](../../models/operations/collect-linked-in-comment-replies-weekly.md) | :heavy_check_mark:                                                                                                    | Current and max weekly usage (null if no weekly cap).                                                                 |