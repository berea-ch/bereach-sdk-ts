# GetMessagesResponse

Conversation messages

## Example Usage

```typescript
import { GetMessagesResponse } from "bereach/models/operations";

let value: GetMessagesResponse = {
  success: true,
  messages: [
    {
      messageUrn: "<value>",
      text: "<value>",
      deliveredAt: 758768,
      senderProfileUrn: "<value>",
      sender: {
        firstName: "Samson",
        lastName: "Trantow",
        profileUrl: "https://everlasting-farm.com",
        headline: "<value>",
        profilePicture: "<value>",
        publicIdentifier: "<value>",
        profileUrn: "<value>",
      },
      attachments: [
        {
          type: "file",
        },
      ],
    },
  ],
  prevCursor: 705334,
  creditsUsed: 656607,
  retryAfter: 791278,
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                    | *true*                                                                                                                       | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `messages`                                                                                                                   | [operations.GetMessagesMessage](../../models/operations/get-messages-message.md)[]                                           | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `prevCursor`                                                                                                                 | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | deliveredAt timestamp (ms) of the oldest message — pass as 'deliveredAt' to load older messages. Null when no more messages. |
| `creditsUsed`                                                                                                                | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                         |
| `retryAfter`                                                                                                                 | *number*                                                                                                                     | :heavy_check_mark:                                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                                         |