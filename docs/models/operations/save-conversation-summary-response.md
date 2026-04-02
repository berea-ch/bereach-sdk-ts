# SaveConversationSummaryResponse

Summary saved

## Example Usage

```typescript
import { SaveConversationSummaryResponse } from "bereach/models/operations";

let value: SaveConversationSummaryResponse = {
  success: true,
  contactId: "<id>",
  summarizedAt: "<value>",
  creditsUsed: 889738,
  retryAfter: 763344,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `contactId`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | Internal contact ID (created if not found)                                           |
| `summarizedAt`                                                                       | *string*                                                                             | :heavy_check_mark:                                                                   | ISO timestamp of when the summary was saved                                          |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |