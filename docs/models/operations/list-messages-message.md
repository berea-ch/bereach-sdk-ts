# ListMessagesMessage

## Example Usage

```typescript
import { ListMessagesMessage } from "bereach/models/operations";

let value: ListMessagesMessage = {
  id: "<id>",
  contactId: "<id>",
  message: "<value>",
  status: "scheduled",
  scheduledSendAt: null,
  sentAt: "<value>",
  campaignSlug: "<value>",
  createdAt: "1704944093147",
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `id`                                                                  | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `contactId`                                                           | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `contactName`                                                         | *string*                                                              | :heavy_minus_sign:                                                    | Contact name (included in list, absent in create)                     |
| `contactLinkedinUrl`                                                  | *string*                                                              | :heavy_minus_sign:                                                    | Contact LinkedIn URL (included in list, absent in create)             |
| `message`                                                             | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `status`                                                              | [operations.MessageStatus](../../models/operations/message-status.md) | :heavy_check_mark:                                                    | N/A                                                                   |
| `scheduledSendAt`                                                     | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `sentAt`                                                              | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `campaignSlug`                                                        | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |
| `errorMessage`                                                        | *string*                                                              | :heavy_minus_sign:                                                    | Error message if status is 'failed'                                   |
| `createdAt`                                                           | *string*                                                              | :heavy_check_mark:                                                    | N/A                                                                   |