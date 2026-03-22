# ScheduledMessage

## Example Usage

```typescript
import { ScheduledMessage } from "bereach/models/operations";

let value: ScheduledMessage = {
  id: "<id>",
  contactId: "<id>",
  message: "<value>",
  status: "sent",
  scheduledSendAt: "<value>",
  sentAt: "<value>",
  campaignSlug: "<value>",
  createdAt: "1713720562023",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `id`                                                                                     | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `contactId`                                                                              | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `contactName`                                                                            | *string*                                                                                 | :heavy_minus_sign:                                                                       | Contact name (included in list, absent in create)                                        |
| `contactLinkedinUrl`                                                                     | *string*                                                                                 | :heavy_minus_sign:                                                                       | Contact LinkedIn URL (included in list, absent in create)                                |
| `message`                                                                                | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `status`                                                                                 | [operations.ScheduledMessageStatus](../../models/operations/scheduled-message-status.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `scheduledSendAt`                                                                        | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `sentAt`                                                                                 | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `campaignSlug`                                                                           | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `errorMessage`                                                                           | *string*                                                                                 | :heavy_minus_sign:                                                                       | Error message if status is 'failed'                                                      |
| `createdAt`                                                                              | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |