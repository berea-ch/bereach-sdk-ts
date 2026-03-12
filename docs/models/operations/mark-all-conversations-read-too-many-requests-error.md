# MarkAllConversationsReadTooManyRequestsError

## Example Usage

```typescript
import { MarkAllConversationsReadTooManyRequestsError } from "bereach/models/operations";

let value: MarkAllConversationsReadTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 777954,
  daily: {
    current: 739770,
    limit: 497084,
  },
  weekly: {
    current: 563755,
    limit: 321050,
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                     | [operations.MarkAllConversationsReadCode](../../models/operations/mark-all-conversations-read-code.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `message`                                                                                                  | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `docs`                                                                                                     | *string*                                                                                                   | :heavy_minus_sign:                                                                                         | N/A                                                                                                        |
| `retryAfter`                                                                                               | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Seconds to wait before retrying.                                                                           |
| `daily`                                                                                                    | [operations.MarkAllConversationsReadDaily](../../models/operations/mark-all-conversations-read-daily.md)   | :heavy_check_mark:                                                                                         | Current and max daily usage (null if no daily cap).                                                        |
| `weekly`                                                                                                   | [operations.MarkAllConversationsReadWeekly](../../models/operations/mark-all-conversations-read-weekly.md) | :heavy_check_mark:                                                                                         | Current and max weekly usage (null if no weekly cap).                                                      |