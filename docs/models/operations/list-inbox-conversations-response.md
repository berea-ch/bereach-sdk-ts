# ListInboxConversationsResponse

Inbox conversations

## Example Usage

```typescript
import { ListInboxConversationsResponse } from "bereach/models/operations";

let value: ListInboxConversationsResponse = {
  success: false,
  conversations: [],
  nextCursor: "<value>",
  creditsUsed: 700190,
  retryAfter: 956075,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `conversations`                                                                                                     | [operations.ListInboxConversationsConversation](../../models/operations/list-inbox-conversations-conversation.md)[] | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `nextCursor`                                                                                                        | *string*                                                                                                            | :heavy_check_mark:                                                                                                  | Cursor for fetching next page                                                                                       |
| `creditsUsed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before making another call of the same type. 0 means no wait needed.                                |