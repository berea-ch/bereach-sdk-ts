# InboxUnreadCountResponse

Unread count

## Example Usage

```typescript
import { InboxUnreadCountResponse } from "bereach/models/operations";

let value: InboxUnreadCountResponse = {
  success: true,
  unreadCount: 606353,
  creditsUsed: 486794,
  retryAfter: 462335,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `unreadCount`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Number of unread conversations/messages                                                                                                   |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.InboxUnreadCountMeta](../../models/operations/inbox-unread-count-meta.md)                                                     | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |