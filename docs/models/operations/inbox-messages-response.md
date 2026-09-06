# InboxMessagesResponse

Conversation messages

## Example Usage

```typescript
import { InboxMessagesResponse } from "bereach/models/operations";

let value: InboxMessagesResponse = {
  success: true,
  messages: [],
  prevCursor: 615925,
  creditsUsed: 376086,
  retryAfter: 88401,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `messages`                                                                                                                                | [operations.InboxMessagesMessage](../../models/operations/inbox-messages-message.md)[]                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `prevCursor`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | deliveredAt timestamp (ms) of the oldest message — pass as 'deliveredAt' to load older messages. Null when no more messages.              |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.InboxMessagesMeta](../../models/operations/inbox-messages-meta.md)                                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |