# ListArchivedConversationsTooManyRequestsError

## Example Usage

```typescript
import { ListArchivedConversationsTooManyRequestsError } from "bereach/models/operations";

let value: ListArchivedConversationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 233570,
  daily: {
    current: 118936,
    limit: 393603,
  },
  weekly: {
    current: 558708,
    limit: 666665,
  },
};
```

## Fields

| Field                                                                                                       | Type                                                                                                        | Required                                                                                                    | Description                                                                                                 |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                      | [operations.ListArchivedConversationsCode](../../models/operations/list-archived-conversations-code.md)     | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `message`                                                                                                   | *string*                                                                                                    | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `docs`                                                                                                      | *string*                                                                                                    | :heavy_minus_sign:                                                                                          | N/A                                                                                                         |
| `retryAfter`                                                                                                | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Seconds to wait before retrying.                                                                            |
| `daily`                                                                                                     | [operations.ListArchivedConversationsDaily](../../models/operations/list-archived-conversations-daily.md)   | :heavy_check_mark:                                                                                          | Current and max daily usage (null if no daily cap).                                                         |
| `weekly`                                                                                                    | [operations.ListArchivedConversationsWeekly](../../models/operations/list-archived-conversations-weekly.md) | :heavy_check_mark:                                                                                          | Current and max weekly usage (null if no weekly cap).                                                       |