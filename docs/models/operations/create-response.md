# CreateResponse

Message created

## Example Usage

```typescript
import { CreateResponse } from "bereach/models/operations";

let value: CreateResponse = {
  success: true,
  message: {
    id: "<id>",
    contactId: "<id>",
    contactName: "<value>",
    contactLinkedinUrl: "https://sad-spring.info",
    message: "<value>",
    status: "scheduled",
    scheduledSendAt: null,
    sentAt: "<value>",
    campaignSlug: "<value>",
    createdAt: "1707703790729",
    updatedAt: "1735635457311",
  },
  creditsUsed: 187133,
  retryAfter: 459940,
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `success`                                                             | *true*                                                                | :heavy_check_mark:                                                    | N/A                                                                   |
| `message`                                                             | [operations.CreateMessage](../../models/operations/create-message.md) | :heavy_check_mark:                                                    | N/A                                                                   |
| `creditsUsed`                                                         | *number*                                                              | :heavy_check_mark:                                                    | Credits consumed (always 0 for workspace operations).                 |
| `retryAfter`                                                          | *number*                                                              | :heavy_check_mark:                                                    | Seconds to wait (always 0 for workspace operations).                  |