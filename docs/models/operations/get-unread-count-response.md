# GetUnreadCountResponse

Unread count

## Example Usage

```typescript
import { GetUnreadCountResponse } from "bereach/models/operations";

let value: GetUnreadCountResponse = {
  success: true,
  unreadCount: 196913,
  creditsUsed: 704186,
  retryAfter: 769109,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `unreadCount`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Number of unread conversations/messages                                              |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |