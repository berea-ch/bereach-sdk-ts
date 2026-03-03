# FindLinkedInConversationConversation

## Example Usage

```typescript
import { FindLinkedInConversationConversation } from "bereach/models/operations";

let value: FindLinkedInConversationConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://understated-dress.org/",
  lastActivityAt: 448742,
  createdAt: 69853,
  read: false,
  unreadCount: 684363,
  groupChat: true,
  participants: [],
  lastMessage: {
    text: "<value>",
    deliveredAt: 277167,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                      | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `conversationUrl`                                                                                                      | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `lastActivityAt`                                                                                                       | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `createdAt`                                                                                                            | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `read`                                                                                                                 | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `unreadCount`                                                                                                          | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `groupChat`                                                                                                            | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `participants`                                                                                                         | [operations.FindLinkedInConversationParticipant](../../models/operations/find-linked-in-conversation-participant.md)[] | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `lastMessage`                                                                                                          | [operations.FindLinkedInConversationLastMessage](../../models/operations/find-linked-in-conversation-last-message.md)  | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |