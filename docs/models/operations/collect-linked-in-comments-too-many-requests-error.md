# CollectLinkedInCommentsTooManyRequestsError

## Example Usage

```typescript
import { CollectLinkedInCommentsTooManyRequestsError } from "bereach/models/operations";

let value: CollectLinkedInCommentsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 718298,
  daily: {
    current: 943422,
    limit: 566808,
  },
  weekly: {
    current: 880892,
    limit: 519310,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.CollectLinkedInCommentsCode](../../models/operations/collect-linked-in-comments-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.CollectLinkedInCommentsDaily](../../models/operations/collect-linked-in-comments-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.CollectLinkedInCommentsWeekly](../../models/operations/collect-linked-in-comments-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |