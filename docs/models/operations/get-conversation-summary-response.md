# GetConversationSummaryResponse

Summary retrieved

## Example Usage

```typescript
import { GetConversationSummaryResponse } from "bereach/models/operations";

let value: GetConversationSummaryResponse = {
  success: true,
  found: true,
  summary: "<value>",
  creditsUsed: 823514,
  retryAfter: 285191,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `found`                                                                              | *boolean*                                                                            | :heavy_check_mark:                                                                   | Whether a contact with a saved summary was found                                     |
| `contactId`                                                                          | *string*                                                                             | :heavy_minus_sign:                                                                   | Internal contact ID — present only when found is true                                |
| `summary`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | The saved conversation summary text, null if none exists                             |
| `summarizedAt`                                                                       | *string*                                                                             | :heavy_minus_sign:                                                                   | ISO timestamp of when the summary was last saved — present only when found is true   |
| `messageCount`                                                                       | *number*                                                                             | :heavy_minus_sign:                                                                   | Message count at the time of summarization — present only when found is true         |
| `conversationUpdatedAt`                                                              | *string*                                                                             | :heavy_minus_sign:                                                                   | Timestamp of last conversation data update — present only when found is true         |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |