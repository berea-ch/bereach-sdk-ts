# ListInboxConversation

## Example Usage

```typescript
import { ListInboxConversation } from "bereach/models/operations";

let value: ListInboxConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://pink-cantaloupe.info",
  lastActivityAt: 638177,
  createdAt: 821754,
  read: true,
  unreadCount: 486134,
  groupChat: false,
  participants: [
    {
      profileUrn: "<value>",
      firstName: "Kris",
      lastName: "Crist",
      profileUrl: "https://infamous-declaration.com/",
      headline: "<value>",
      profilePicture: "<value>",
      publicIdentifier: "<value>",
    },
  ],
  lastMessage: {
    text: "<value>",
    deliveredAt: 329725,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                      | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `conversationUrl`                                                                      | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `lastActivityAt`                                                                       | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `createdAt`                                                                            | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `read`                                                                                 | *boolean*                                                                              | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `unreadCount`                                                                          | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `groupChat`                                                                            | *boolean*                                                                              | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `participants`                                                                         | [operations.ListInboxParticipant](../../models/operations/list-inbox-participant.md)[] | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `lastMessage`                                                                          | [operations.ListInboxLastMessage](../../models/operations/list-inbox-last-message.md)  | :heavy_check_mark:                                                                     | N/A                                                                                    |