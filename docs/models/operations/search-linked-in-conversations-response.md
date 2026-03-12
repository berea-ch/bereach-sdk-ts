# SearchLinkedInConversationsResponse

Matching conversations

## Example Usage

```typescript
import { SearchLinkedInConversationsResponse } from "bereach/models/operations";

let value: SearchLinkedInConversationsResponse = {
  success: true,
  conversations: [],
  nextCursor: "<value>",
  creditsUsed: 982398,
  retryAfter: 206067,
};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                      | *true*                                                                                                                         | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `conversations`                                                                                                                | [operations.SearchLinkedInConversationsConversation](../../models/operations/search-linked-in-conversations-conversation.md)[] | :heavy_check_mark:                                                                                                             | N/A                                                                                                                            |
| `nextCursor`                                                                                                                   | *string*                                                                                                                       | :heavy_check_mark:                                                                                                             | Cursor for fetching next page                                                                                                  |
| `creditsUsed`                                                                                                                  | *number*                                                                                                                       | :heavy_check_mark:                                                                                                             | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                           |
| `retryAfter`                                                                                                                   | *number*                                                                                                                       | :heavy_check_mark:                                                                                                             | Seconds to wait before making another call of the same type. 0 means no wait needed.                                           |