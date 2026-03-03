# FindLinkedInConversationResponse

Conversation found (or not)

## Example Usage

```typescript
import { FindLinkedInConversationResponse } from "bereach/models/operations";

let value: FindLinkedInConversationResponse = {
  success: true,
  found: false,
  conversation: {
    conversationUrn: "<value>",
    conversationUrl: "https://altruistic-ruin.org/",
    lastActivityAt: 605090,
    createdAt: 838394,
    read: true,
    unreadCount: 274029,
    groupChat: true,
    participants: [
      {
        profileUrn: "<value>",
        firstName: "Itzel",
        lastName: "Swaniawski",
        profileUrl: "https://bouncy-merit.biz",
        headline: "<value>",
        profilePicture: "<value>",
      },
    ],
    lastMessage: {
      text: "<value>",
      deliveredAt: 277167,
      senderProfileUrn: "<value>",
    },
  },
  messages: [
    {
      messageUrn: "<value>",
      text: "<value>",
      deliveredAt: 219906,
      senderProfileUrn: "<value>",
      sender: {
        firstName: "Elijah",
        lastName: "Ernser",
        profileUrl: "https://webbed-stock.net/",
        headline: "<value>",
        profilePicture: "<value>",
      },
      attachments: [],
    },
  ],
  creditsUsed: 517167,
  retryAfter: 282123,
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                              | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `found`                                                                                                                | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `conversation`                                                                                                         | [operations.FindLinkedInConversationConversation](../../models/operations/find-linked-in-conversation-conversation.md) | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `messages`                                                                                                             | [operations.FindLinkedInConversationMessage](../../models/operations/find-linked-in-conversation-message.md)[]         | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `creditsUsed`                                                                                                          | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                   |
| `retryAfter`                                                                                                           | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Seconds to wait before making another call of the same type. 0 means no wait needed.                                   |