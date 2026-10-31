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

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `unreadCount`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Number of unread conversations/messages                                                                                           |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |