# ListStarredConversationsResponse

Starred conversations

## Example Usage

```typescript
import { ListStarredConversationsResponse } from "bereach/models/operations";

let value: ListStarredConversationsResponse = {
  success: true,
  conversations: [],
  nextCursor: null,
  creditsUsed: 930288,
  retryAfter: 638513,
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                               | *true*                                                                                                                  | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `conversations`                                                                                                         | [operations.ListStarredConversationsConversation](../../models/operations/list-starred-conversations-conversation.md)[] | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `nextCursor`                                                                                                            | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | Cursor for fetching next page                                                                                           |
| `creditsUsed`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                    |
| `retryAfter`                                                                                                            | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Seconds to wait before making another call of the same type. 0 means no wait needed.                                    |