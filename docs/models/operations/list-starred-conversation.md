# ListStarredConversation

## Example Usage

```typescript
import { ListStarredConversation } from "bereach/models/operations";

let value: ListStarredConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://delectable-brook.net",
  lastActivityAt: 375676,
  createdAt: 261811,
  read: true,
  unreadCount: 369361,
  groupChat: false,
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
  lastMessage: null,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `conversationUrn`                                                                          | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `conversationUrl`                                                                          | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastActivityAt`                                                                           | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `createdAt`                                                                                | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `read`                                                                                     | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `unreadCount`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `groupChat`                                                                                | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `participants`                                                                             | [operations.ListStarredParticipant](../../models/operations/list-starred-participant.md)[] | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastMessage`                                                                              | [operations.ListStarredLastMessage](../../models/operations/list-starred-last-message.md)  | :heavy_check_mark:                                                                         | N/A                                                                                        |