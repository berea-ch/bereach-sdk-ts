# InboxSearchResponse

Matching conversations

## Example Usage

```typescript
import { InboxSearchResponse } from "bereach/models/operations";

let value: InboxSearchResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://fond-replacement.info",
      lastActivityAt: 567072,
      createdAt: 461637,
      read: true,
      unreadCount: 446046,
      groupChat: true,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Rosalinda",
          lastName: "Schroeder",
          profileUrl: "https://noteworthy-testing.com/",
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: "<value>",
        deliveredAt: 816412,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 42645,
  retryAfter: 546872,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `conversations`                                                                                                                           | [operations.InboxSearchConversation](../../models/operations/inbox-search-conversation.md)[]                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `nextCursor`                                                                                                                              | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Cursor for fetching next page                                                                                                             |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.InboxSearchMeta](../../models/operations/inbox-search-meta.md)                                                                | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |