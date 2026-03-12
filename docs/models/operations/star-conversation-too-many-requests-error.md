# StarConversationTooManyRequestsError

## Example Usage

```typescript
import { StarConversationTooManyRequestsError } from "bereach/models/operations";

let value: StarConversationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 300258,
  daily: {
    current: 164871,
    limit: 29228,
  },
  weekly: {
    current: 232913,
    limit: 51984,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `code`                                                                                   | [operations.StarConversationCode](../../models/operations/star-conversation-code.md)     | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `message`                                                                                | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `docs`                                                                                   | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before retrying.                                                         |
| `daily`                                                                                  | [operations.StarConversationDaily](../../models/operations/star-conversation-daily.md)   | :heavy_check_mark:                                                                       | Current and max daily usage (null if no daily cap).                                      |
| `weekly`                                                                                 | [operations.StarConversationWeekly](../../models/operations/star-conversation-weekly.md) | :heavy_check_mark:                                                                       | Current and max weekly usage (null if no weekly cap).                                    |