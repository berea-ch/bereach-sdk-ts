# UnstarConversationTooManyRequestsError

## Example Usage

```typescript
import { UnstarConversationTooManyRequestsError } from "bereach/models/operations";

let value: UnstarConversationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 303854,
  daily: {
    current: 909959,
    limit: 14537,
  },
  weekly: {
    current: 835634,
    limit: 561606,
  },
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `code`                                                                                       | [operations.UnstarConversationCode](../../models/operations/unstar-conversation-code.md)     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `message`                                                                                    | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `docs`                                                                                       | *string*                                                                                     | :heavy_minus_sign:                                                                           | N/A                                                                                          |
| `retryAfter`                                                                                 | *number*                                                                                     | :heavy_check_mark:                                                                           | Seconds to wait before retrying.                                                             |
| `daily`                                                                                      | [operations.UnstarConversationDaily](../../models/operations/unstar-conversation-daily.md)   | :heavy_check_mark:                                                                           | Current and max daily usage (null if no daily cap).                                          |
| `weekly`                                                                                     | [operations.UnstarConversationWeekly](../../models/operations/unstar-conversation-weekly.md) | :heavy_check_mark:                                                                           | Current and max weekly usage (null if no weekly cap).                                        |