# ListStarredResponse

Starred conversations

## Example Usage

```typescript
import { ListStarredResponse } from "bereach/models/operations";

let value: ListStarredResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://insignificant-guide.net",
      lastActivityAt: 369055,
      createdAt: 793954,
      read: false,
      unreadCount: 311439,
      groupChat: true,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Mia",
          lastName: "Howell",
          profileUrl: "https://bruised-phrase.net/",
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: null,
        },
      ],
      lastMessage: {
        text: "<value>",
        deliveredAt: 696594,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 245876,
  retryAfter: 103163,
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `success`                                                                                    | *true*                                                                                       | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `conversations`                                                                              | [operations.ListStarredConversation](../../models/operations/list-starred-conversation.md)[] | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `nextCursor`                                                                                 | *string*                                                                                     | :heavy_check_mark:                                                                           | Cursor for fetching next page                                                                |
| `creditsUsed`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).         |
| `retryAfter`                                                                                 | *number*                                                                                     | :heavy_check_mark:                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.         |