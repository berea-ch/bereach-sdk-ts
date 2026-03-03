# GetConversationMessagesResponse

Conversation messages

## Example Usage

```typescript
import { GetConversationMessagesResponse } from "bereach/models/operations";

let value: GetConversationMessagesResponse = {
  success: false,
  messages: [
    {
      messageUrn: "<value>",
      text: "<value>",
      deliveredAt: 283070,
      senderProfileUrn: "<value>",
      sender: {
        firstName: "Kieran",
        lastName: "Jenkins",
        profileUrl: "https://speedy-schnitzel.com",
        headline: "<value>",
        profilePicture: "<value>",
      },
      attachments: [
        {
          type: "image",
        },
      ],
    },
  ],
  prevCursor: null,
  creditsUsed: 455352,
  retryAfter: 754214,
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                    | *boolean*                                                                                                                    | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `messages`                                                                                                                   | [operations.GetConversationMessagesMessage](../../models/operations/get-conversation-messages-message.md)[]                  | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `prevCursor`                                                                                                                 | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | deliveredAt timestamp (ms) of the oldest message — pass as 'deliveredAt' to load older messages. Null when no more messages. |
| `creditsUsed`                                                                                                                | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                         |
| `retryAfter`                                                                                                                 | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                                         |