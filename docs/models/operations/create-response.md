# CreateResponse

Message created

## Example Usage

```typescript
import { CreateResponse } from "bereach/models/operations";

let value: CreateResponse = {
  success: true,
  scheduledMessage: {
    id: "<id>",
    contactId: "<id>",
    message: "<value>",
    status: "scheduled",
    scheduledSendAt: "<value>",
    sentAt: "<value>",
    campaignSlug: "<value>",
    createdAt: "1730666516543",
  },
  creditsUsed: 433306,
  retryAfter: 181374,
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `success`                                                                   | *true*                                                                      | :heavy_check_mark:                                                          | N/A                                                                         |
| `scheduledMessage`                                                          | [operations.ScheduledMessage](../../models/operations/scheduled-message.md) | :heavy_check_mark:                                                          | N/A                                                                         |
| `creditsUsed`                                                               | *number*                                                                    | :heavy_check_mark:                                                          | Credits consumed (always 0 for workspace operations).                       |
| `retryAfter`                                                                | *number*                                                                    | :heavy_check_mark:                                                          | Seconds to wait (always 0 for workspace operations).                        |