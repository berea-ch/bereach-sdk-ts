# SearchLinkedInConversationsConversation

## Example Usage

```typescript
import { SearchLinkedInConversationsConversation } from "bereach/models/operations";

let value: SearchLinkedInConversationsConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://noxious-jet.com/",
  lastActivityAt: 903964,
  createdAt: 62700,
  read: true,
  unreadCount: 366637,
  groupChat: true,
  participants: [
    {
      profileUrn: "<value>",
      firstName: "Freddy",
      lastName: "DuBuque",
      profileUrl: "https://closed-appliance.net",
      headline: "<value>",
      profilePicture: "<value>",
    },
  ],
  lastMessage: {
    text: "<value>",
    deliveredAt: 123335,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                            | *string*                                                                                                                     | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `conversationUrl`                                                                                                            | *string*                                                                                                                     | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `lastActivityAt`                                                                                                             | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `createdAt`                                                                                                                  | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `read`                                                                                                                       | *boolean*                                                                                                                    | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `unreadCount`                                                                                                                | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `groupChat`                                                                                                                  | *boolean*                                                                                                                    | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `participants`                                                                                                               | [operations.SearchLinkedInConversationsParticipant](../../models/operations/search-linked-in-conversations-participant.md)[] | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `lastMessage`                                                                                                                | [operations.SearchLinkedInConversationsLastMessage](../../models/operations/search-linked-in-conversations-last-message.md)  | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |