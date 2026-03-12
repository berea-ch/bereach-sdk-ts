# ListInboxConversationsTooManyRequestsError

## Example Usage

```typescript
import { ListInboxConversationsTooManyRequestsError } from "bereach/models/operations";

let value: ListInboxConversationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 714385,
  daily: {
    current: 136579,
    limit: 480060,
  },
  weekly: {
    current: 962635,
    limit: 648035,
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `code`                                                                                                | [operations.ListInboxConversationsCode](../../models/operations/list-inbox-conversations-code.md)     | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `message`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `docs`                                                                                                | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `retryAfter`                                                                                          | *number*                                                                                              | :heavy_check_mark:                                                                                    | Seconds to wait before retrying.                                                                      |
| `daily`                                                                                               | [operations.ListInboxConversationsDaily](../../models/operations/list-inbox-conversations-daily.md)   | :heavy_check_mark:                                                                                    | Current and max daily usage (null if no daily cap).                                                   |
| `weekly`                                                                                              | [operations.ListInboxConversationsWeekly](../../models/operations/list-inbox-conversations-weekly.md) | :heavy_check_mark:                                                                                    | Current and max weekly usage (null if no weekly cap).                                                 |