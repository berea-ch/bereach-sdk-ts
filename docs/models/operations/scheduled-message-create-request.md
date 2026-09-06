# ScheduledMessageCreateRequest

## Example Usage

```typescript
import { ScheduledMessageCreateRequest } from "bereach/models/operations";

let value: ScheduledMessageCreateRequest = {
  contactId: "<id>",
  message: "<value>",
};
```

## Fields

| Field                                                                                                                       | Type                                                                                                                        | Required                                                                                                                    | Description                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| `contactId`                                                                                                                 | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | Internal contact ID                                                                                                         |
| `message`                                                                                                                   | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | DM text                                                                                                                     |
| `status`                                                                                                                    | [operations.StatusRequest](../../models/operations/status-request.md)                                                       | :heavy_minus_sign:                                                                                                          | Default 'draft'                                                                                                             |
| `scheduledSendAt`                                                                                                           | *string*                                                                                                                    | :heavy_minus_sign:                                                                                                          | ISO datetime for auto-send                                                                                                  |
| `campaignSlug`                                                                                                              | *string*                                                                                                                    | :heavy_minus_sign:                                                                                                          | Which list to file the draft under. Omit it: the draft is filed with the person it is for, which is what a chat turn wants. |