# InboxListResponse

Inbox conversations

## Example Usage

```typescript
import { InboxListResponse } from "bereach/models/operations";

let value: InboxListResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://queasy-gray.biz",
      lastActivityAt: 291893,
      createdAt: 237397,
      read: true,
      unreadCount: 274144,
      groupChat: false,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Casimir",
          lastName: "Champlin",
          profileUrl: null,
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: null,
        deliveredAt: 441255,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 630398,
  retryAfter: 801573,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `conversations`                                                                                                                           | [operations.InboxListConversation](../../models/operations/inbox-list-conversation.md)[]                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `nextCursor`                                                                                                                              | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Cursor for fetching next page                                                                                                             |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.InboxListMeta](../../models/operations/inbox-list-meta.md)                                                                    | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |