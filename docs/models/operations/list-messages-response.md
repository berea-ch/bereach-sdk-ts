# ListMessagesResponse

Messages list

## Example Usage

```typescript
import { ListMessagesResponse } from "bereach/models/operations";

let value: ListMessagesResponse = {
  success: true,
  messages: [
    {
      id: "<id>",
      contactId: "<id>",
      message: "<value>",
      status: "failed",
      scheduledSendAt: "<value>",
      sentAt: "<value>",
      campaignSlug: "<value>",
      createdAt: "1708931886392",
    },
  ],
  total: 280101,
  limit: 342012,
  offset: 88352,
  creditsUsed: 163465,
  retryAfter: 83969,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `messages`                                                                           | [operations.ListMessagesMessage](../../models/operations/list-messages-message.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `limit`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `offset`                                                                             | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed (always 0 for workspace operations).                                |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait (always 0 for workspace operations).                                 |