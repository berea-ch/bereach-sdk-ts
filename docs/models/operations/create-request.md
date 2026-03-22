# CreateRequest

## Example Usage

```typescript
import { CreateRequest } from "bereach/models/operations";

let value: CreateRequest = {
  contactId: "<id>",
  message: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `contactId`                                                                        | *string*                                                                           | :heavy_check_mark:                                                                 | Internal contact ID                                                                |
| `message`                                                                          | *string*                                                                           | :heavy_check_mark:                                                                 | DM text                                                                            |
| `status`                                                                           | [operations.CreateStatusRequest](../../models/operations/create-status-request.md) | :heavy_minus_sign:                                                                 | Default 'draft'                                                                    |
| `scheduledSendAt`                                                                  | *string*                                                                           | :heavy_minus_sign:                                                                 | ISO datetime for auto-send                                                         |
| `campaignSlug`                                                                     | *string*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |