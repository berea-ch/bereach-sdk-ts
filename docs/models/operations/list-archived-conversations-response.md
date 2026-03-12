# ListArchivedConversationsResponse

Archived conversations

## Example Usage

```typescript
import { ListArchivedConversationsResponse } from "bereach/models/operations";

let value: ListArchivedConversationsResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://exotic-gymnast.biz",
      lastActivityAt: 10992,
      createdAt: 430649,
      read: true,
      unreadCount: 485250,
      groupChat: false,
      participants: [],
      lastMessage: {
        text: "<value>",
        deliveredAt: 58159,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 928021,
  retryAfter: 663930,
};
```

## Fields

| Field                                                                                                                     | Type                                                                                                                      | Required                                                                                                                  | Description                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                 | *true*                                                                                                                    | :heavy_check_mark:                                                                                                        | N/A                                                                                                                       |
| `conversations`                                                                                                           | [operations.ListArchivedConversationsConversation](../../models/operations/list-archived-conversations-conversation.md)[] | :heavy_check_mark:                                                                                                        | N/A                                                                                                                       |
| `nextCursor`                                                                                                              | *string*                                                                                                                  | :heavy_check_mark:                                                                                                        | Cursor for fetching next page                                                                                             |
| `creditsUsed`                                                                                                             | *number*                                                                                                                  | :heavy_check_mark:                                                                                                        | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                      |
| `retryAfter`                                                                                                              | *number*                                                                                                                  | :heavy_check_mark:                                                                                                        | Seconds to wait before making another call of the same type. 0 means no wait needed.                                      |