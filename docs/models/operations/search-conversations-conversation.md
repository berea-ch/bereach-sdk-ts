# SearchConversationsConversation

## Example Usage

```typescript
import { SearchConversationsConversation } from "bereach/models/operations";

let value: SearchConversationsConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://hefty-comestible.org",
  lastActivityAt: 151988,
  createdAt: 914634,
  read: true,
  unreadCount: 832969,
  groupChat: false,
  participants: [],
  lastMessage: {
    text: "<value>",
    deliveredAt: 508975,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                          | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `conversationUrl`                                                                                          | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `lastActivityAt`                                                                                           | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `createdAt`                                                                                                | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `read`                                                                                                     | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `unreadCount`                                                                                              | *number*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `groupChat`                                                                                                | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `participants`                                                                                             | [operations.SearchConversationsParticipant](../../models/operations/search-conversations-participant.md)[] | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `lastMessage`                                                                                              | [operations.SearchConversationsLastMessage](../../models/operations/search-conversations-last-message.md)  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |