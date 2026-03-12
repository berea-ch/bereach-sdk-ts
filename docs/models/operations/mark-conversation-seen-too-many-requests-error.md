# MarkConversationSeenTooManyRequestsError

## Example Usage

```typescript
import { MarkConversationSeenTooManyRequestsError } from "bereach/models/operations";

let value: MarkConversationSeenTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 939054,
  daily: {
    current: 420908,
    limit: 518262,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `code`                                                                                            | [operations.MarkConversationSeenCode](../../models/operations/mark-conversation-seen-code.md)     | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `message`                                                                                         | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `docs`                                                                                            | *string*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `retryAfter`                                                                                      | *number*                                                                                          | :heavy_check_mark:                                                                                | Seconds to wait before retrying.                                                                  |
| `daily`                                                                                           | [operations.MarkConversationSeenDaily](../../models/operations/mark-conversation-seen-daily.md)   | :heavy_check_mark:                                                                                | Current and max daily usage (null if no daily cap).                                               |
| `weekly`                                                                                          | [operations.MarkConversationSeenWeekly](../../models/operations/mark-conversation-seen-weekly.md) | :heavy_check_mark:                                                                                | Current and max weekly usage (null if no weekly cap).                                             |