# ListInboxConversationsResponse

Inbox conversations

## Example Usage

```typescript
import { ListInboxConversationsResponse } from "bereach/models/operations";

let value: ListInboxConversationsResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://shabby-premier.org/",
      lastActivityAt: 884879,
      createdAt: 420400,
      read: false,
      unreadCount: 405506,
      groupChat: false,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Bianka",
          lastName: "D'Amore",
          profileUrl: "https://exalted-approach.name",
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: "<value>",
        deliveredAt: 394931,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 326793,
  retryAfter: 123536,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                           | *true*                                                                                                              | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `conversations`                                                                                                     | [operations.ListInboxConversationsConversation](../../models/operations/list-inbox-conversations-conversation.md)[] | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `nextCursor`                                                                                                        | *string*                                                                                                            | :heavy_check_mark:                                                                                                  | Cursor for fetching next page                                                                                       |
| `creditsUsed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before making another call of the same type. 0 means no wait needed.                                |