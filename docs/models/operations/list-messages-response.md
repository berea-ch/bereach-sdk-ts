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
      contactName: "<value>",
      contactLinkedinUrl: "https://lucky-cinema.biz/",
      message: "<value>",
      status: "sending",
      scheduledSendAt: null,
      sentAt: "<value>",
      campaignSlug: null,
      createdAt: "1731133287979",
      updatedAt: "1735655390716",
    },
  ],
  pagination: {
    limit: 3162.79,
    offset: 7688.81,
    total: 5107.88,
  },
  creditsUsed: 105695,
  retryAfter: 738933,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `messages`                                                                               | [operations.ListMessagesMessage](../../models/operations/list-messages-message.md)[]     | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `pagination`                                                                             | [operations.ListMessagesPagination](../../models/operations/list-messages-pagination.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed (always 0 for workspace operations).                                    |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait (always 0 for workspace operations).                                     |