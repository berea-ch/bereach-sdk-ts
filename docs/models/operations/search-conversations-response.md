# SearchConversationsResponse

Matching conversations

## Example Usage

```typescript
import { SearchConversationsResponse } from "bereach/models/operations";

let value: SearchConversationsResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://quarrelsome-airline.name",
      lastActivityAt: 444703,
      createdAt: 792922,
      read: false,
      unreadCount: 338147,
      groupChat: false,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Woodrow",
          lastName: "Dach-Hermann",
          profileUrl: "https://ordinary-creature.org",
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: "<value>",
        deliveredAt: 508975,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 996109,
  retryAfter: 851607,
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                    | *true*                                                                                                       | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `conversations`                                                                                              | [operations.SearchConversationsConversation](../../models/operations/search-conversations-conversation.md)[] | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `nextCursor`                                                                                                 | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Cursor for fetching next page                                                                                |
| `creditsUsed`                                                                                                | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                         |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                         |