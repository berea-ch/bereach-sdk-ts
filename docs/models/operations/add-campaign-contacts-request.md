# AddCampaignContactsRequest

## Example Usage

```typescript
import { AddCampaignContactsRequest } from "bereach/models/operations";

let value: AddCampaignContactsRequest = {
  campaignId: "<id>",
  body: {
    contacts: [],
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Campaign ID                                                                                                |
| `body`                                                                                                     | [operations.AddCampaignContactsRequestBody](../../models/operations/add-campaign-contacts-request-body.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |