# GetConversationMessagesTooManyRequestsError

## Example Usage

```typescript
import { GetConversationMessagesTooManyRequestsError } from "bereach/models/operations";

let value: GetConversationMessagesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 511412,
  daily: {
    current: 850370,
    limit: 141512,
  },
  weekly: {
    current: 780249,
    limit: 990186,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                  | [operations.GetConversationMessagesCode](../../models/operations/get-conversation-messages-code.md)     | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `message`                                                                                               | *string*                                                                                                | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `docs`                                                                                                  | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `retryAfter`                                                                                            | *number*                                                                                                | :heavy_check_mark:                                                                                      | Seconds to wait before retrying.                                                                        |
| `daily`                                                                                                 | [operations.GetConversationMessagesDaily](../../models/operations/get-conversation-messages-daily.md)   | :heavy_check_mark:                                                                                      | Current and max daily usage (null if no daily cap).                                                     |
| `weekly`                                                                                                | [operations.GetConversationMessagesWeekly](../../models/operations/get-conversation-messages-weekly.md) | :heavy_check_mark:                                                                                      | Current and max weekly usage (null if no weekly cap).                                                   |