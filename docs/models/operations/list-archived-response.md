# ListArchivedResponse

Archived conversations

## Example Usage

```typescript
import { ListArchivedResponse } from "bereach/models/operations";

let value: ListArchivedResponse = {
  success: true,
  conversations: [],
  nextCursor: "<value>",
  creditsUsed: 416687,
  retryAfter: 723145,
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `success`                                                                                      | *true*                                                                                         | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `conversations`                                                                                | [operations.ListArchivedConversation](../../models/operations/list-archived-conversation.md)[] | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `nextCursor`                                                                                   | *string*                                                                                       | :heavy_check_mark:                                                                             | Cursor for fetching next page                                                                  |
| `creditsUsed`                                                                                  | *number*                                                                                       | :heavy_check_mark:                                                                             | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).           |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before making another call of the same type. 0 means no wait needed.           |