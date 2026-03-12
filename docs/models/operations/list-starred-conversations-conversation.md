# ListStarredConversationsConversation

## Example Usage

```typescript
import { ListStarredConversationsConversation } from "bereach/models/operations";

let value: ListStarredConversationsConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://foolhardy-gown.name/",
  lastActivityAt: 44675,
  createdAt: 521204,
  read: false,
  unreadCount: 796322,
  groupChat: false,
  participants: [
    {
      profileUrn: "<value>",
      firstName: "Vladimir",
      lastName: "Balistreri",
      profileUrl: "https://instructive-lashes.com",
      headline: "<value>",
      profilePicture: "<value>",
    },
  ],
  lastMessage: {
    text: "<value>",
    deliveredAt: 495495,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                     | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `conversationUrl`                                                                                                     | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `lastActivityAt`                                                                                                      | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `createdAt`                                                                                                           | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `read`                                                                                                                | *boolean*                                                                                                             | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `unreadCount`                                                                                                         | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `groupChat`                                                                                                           | *boolean*                                                                                                             | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `participants`                                                                                                        | [operations.ListStarredConversationsParticipant](../../models/operations/list-starred-conversations-participant.md)[] | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `lastMessage`                                                                                                         | [operations.ListStarredConversationsLastMessage](../../models/operations/list-starred-conversations-last-message.md)  | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |