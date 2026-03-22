# ListArchivedConversation

## Example Usage

```typescript
import { ListArchivedConversation } from "bereach/models/operations";

let value: ListArchivedConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://pretty-case.name",
  lastActivityAt: 257642,
  createdAt: 92632,
  read: false,
  unreadCount: 536509,
  groupChat: false,
  participants: [],
  lastMessage: {
    text: "<value>",
    deliveredAt: 375756,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                            | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `conversationUrl`                                                                            | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `lastActivityAt`                                                                             | *number*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `createdAt`                                                                                  | *number*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `read`                                                                                       | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `unreadCount`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `groupChat`                                                                                  | *boolean*                                                                                    | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `participants`                                                                               | [operations.ListArchivedParticipant](../../models/operations/list-archived-participant.md)[] | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `lastMessage`                                                                                | [operations.ListArchivedLastMessage](../../models/operations/list-archived-last-message.md)  | :heavy_check_mark:                                                                           | N/A                                                                                          |