# CreateMessage

## Example Usage

```typescript
import { CreateMessage } from "bereach/models/operations";

let value: CreateMessage = {
  id: "<id>",
  contactId: "<id>",
  contactName: "<value>",
  contactLinkedinUrl: "https://livid-sailor.net/",
  message: "<value>",
  status: "sent",
  scheduledSendAt: "<value>",
  sentAt: "<value>",
  campaignSlug: "<value>",
  createdAt: "1731478168637",
  updatedAt: "1735668646881",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `contactId`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `contactName`                                                                        | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `contactLinkedinUrl`                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `message`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `status`                                                                             | [operations.CreateStatusResponse](../../models/operations/create-status-response.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `scheduledSendAt`                                                                    | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `sentAt`                                                                             | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `campaignSlug`                                                                       | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `createdAt`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `updatedAt`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |