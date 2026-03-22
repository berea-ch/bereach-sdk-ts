# ListMessagesMessage

## Example Usage

```typescript
import { ListMessagesMessage } from "bereach/models/operations";

let value: ListMessagesMessage = {
  id: "<id>",
  contactId: "<id>",
  contactName: "<value>",
  contactLinkedinUrl: null,
  message: "<value>",
  status: "cancelled",
  scheduledSendAt: "<value>",
  sentAt: null,
  campaignSlug: "<value>",
  createdAt: "1715398478550",
  updatedAt: "1735684574034",
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `contactId`                                                                                       | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `contactName`                                                                                     | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `contactLinkedinUrl`                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `message`                                                                                         | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `status`                                                                                          | [operations.ListMessagesStatusResponse](../../models/operations/list-messages-status-response.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `scheduledSendAt`                                                                                 | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `sentAt`                                                                                          | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `campaignSlug`                                                                                    | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `createdAt`                                                                                       | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `updatedAt`                                                                                       | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |