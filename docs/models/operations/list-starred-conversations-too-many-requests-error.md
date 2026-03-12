# ListStarredConversationsTooManyRequestsError

## Example Usage

```typescript
import { ListStarredConversationsTooManyRequestsError } from "bereach/models/operations";

let value: ListStarredConversationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 157832,
  daily: {
    current: 409712,
    limit: 179447,
  },
  weekly: {
    current: 908099,
    limit: 752765,
  },
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                    | [operations.ListStarredConversationsCode](../../models/operations/list-starred-conversations-code.md)     | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `message`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `docs`                                                                                                    | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `retryAfter`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Seconds to wait before retrying.                                                                          |
| `daily`                                                                                                   | [operations.ListStarredConversationsDaily](../../models/operations/list-starred-conversations-daily.md)   | :heavy_check_mark:                                                                                        | Current and max daily usage (null if no daily cap).                                                       |
| `weekly`                                                                                                  | [operations.ListStarredConversationsWeekly](../../models/operations/list-starred-conversations-weekly.md) | :heavy_check_mark:                                                                                        | Current and max weekly usage (null if no weekly cap).                                                     |