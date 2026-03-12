# SearchLinkedInConversationsTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInConversationsTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInConversationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 226791,
  daily: {
    current: 527562,
    limit: 176143,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                           | [operations.SearchLinkedInConversationsCode](../../models/operations/search-linked-in-conversations-code.md)     | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `message`                                                                                                        | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `docs`                                                                                                           | *string*                                                                                                         | :heavy_minus_sign:                                                                                               | N/A                                                                                                              |
| `retryAfter`                                                                                                     | *number*                                                                                                         | :heavy_check_mark:                                                                                               | Seconds to wait before retrying.                                                                                 |
| `daily`                                                                                                          | [operations.SearchLinkedInConversationsDaily](../../models/operations/search-linked-in-conversations-daily.md)   | :heavy_check_mark:                                                                                               | Current and max daily usage (null if no daily cap).                                                              |
| `weekly`                                                                                                         | [operations.SearchLinkedInConversationsWeekly](../../models/operations/search-linked-in-conversations-weekly.md) | :heavy_check_mark:                                                                                               | Current and max weekly usage (null if no weekly cap).                                                            |