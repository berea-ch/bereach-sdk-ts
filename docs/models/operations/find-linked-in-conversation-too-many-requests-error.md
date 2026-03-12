# FindLinkedInConversationTooManyRequestsError

## Example Usage

```typescript
import { FindLinkedInConversationTooManyRequestsError } from "bereach/models/operations";

let value: FindLinkedInConversationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 679093,
  daily: null,
  weekly: {
    current: 793832,
    limit: 395232,
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                     | [operations.FindLinkedInConversationCode](../../models/operations/find-linked-in-conversation-code.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `message`                                                                                                  | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `docs`                                                                                                     | *string*                                                                                                   | :heavy_minus_sign:                                                                                         | N/A                                                                                                        |
| `retryAfter`                                                                                               | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Seconds to wait before retrying.                                                                           |
| `daily`                                                                                                    | [operations.FindLinkedInConversationDaily](../../models/operations/find-linked-in-conversation-daily.md)   | :heavy_check_mark:                                                                                         | Current and max daily usage (null if no daily cap).                                                        |
| `weekly`                                                                                                   | [operations.FindLinkedInConversationWeekly](../../models/operations/find-linked-in-conversation-weekly.md) | :heavy_check_mark:                                                                                         | Current and max weekly usage (null if no weekly cap).                                                      |