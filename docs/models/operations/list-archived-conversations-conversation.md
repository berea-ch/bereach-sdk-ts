# ListArchivedConversationsConversation

## Example Usage

```typescript
import { ListArchivedConversationsConversation } from "bereach/models/operations";

let value: ListArchivedConversationsConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://ecstatic-individual.com",
  lastActivityAt: 75365,
  createdAt: 193041,
  read: false,
  unreadCount: 95717,
  groupChat: false,
  participants: [
    {
      profileUrn: "<value>",
      firstName: "Vladimir",
      lastName: "Bashirian",
      profileUrl: "https://pleasing-integer.org/",
      headline: "<value>",
      profilePicture: "<value>",
    },
  ],
  lastMessage: {
    text: "<value>",
    deliveredAt: 58159,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                       | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `conversationUrl`                                                                                                       | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `lastActivityAt`                                                                                                        | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `createdAt`                                                                                                             | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `read`                                                                                                                  | *boolean*                                                                                                               | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `unreadCount`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `groupChat`                                                                                                             | *boolean*                                                                                                               | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `participants`                                                                                                          | [operations.ListArchivedConversationsParticipant](../../models/operations/list-archived-conversations-participant.md)[] | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `lastMessage`                                                                                                           | [operations.ListArchivedConversationsLastMessage](../../models/operations/list-archived-conversations-last-message.md)  | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |