# ListInboxConversationsConversation

## Example Usage

```typescript
import { ListInboxConversationsConversation } from "bereach/models/operations";

let value: ListInboxConversationsConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://medium-polarisation.net",
  lastActivityAt: 764567,
  createdAt: 740051,
  read: false,
  unreadCount: 856321,
  groupChat: true,
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
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                 | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `conversationUrl`                                                                                                 | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `lastActivityAt`                                                                                                  | *number*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `createdAt`                                                                                                       | *number*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `read`                                                                                                            | *boolean*                                                                                                         | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `unreadCount`                                                                                                     | *number*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `groupChat`                                                                                                       | *boolean*                                                                                                         | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `participants`                                                                                                    | [operations.ListInboxConversationsParticipant](../../models/operations/list-inbox-conversations-participant.md)[] | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `lastMessage`                                                                                                     | [operations.ListInboxConversationsLastMessage](../../models/operations/list-inbox-conversations-last-message.md)  | :heavy_check_mark:                                                                                                | N/A                                                                                                               |