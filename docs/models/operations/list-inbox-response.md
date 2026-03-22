# ListInboxResponse

Inbox conversations

## Example Usage

```typescript
import { ListInboxResponse } from "bereach/models/operations";

let value: ListInboxResponse = {
  success: true,
  conversations: [],
  nextCursor: "<value>",
  creditsUsed: 908021,
  retryAfter: 795842,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `conversations`                                                                          | [operations.ListInboxConversation](../../models/operations/list-inbox-conversation.md)[] | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `nextCursor`                                                                             | *string*                                                                                 | :heavy_check_mark:                                                                       | Cursor for fetching next page                                                            |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).     |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before making another call of the same type. 0 means no wait needed.     |