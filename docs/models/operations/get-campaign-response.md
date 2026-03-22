# GetCampaignResponse

Campaign details

## Example Usage

```typescript
import { GetCampaignResponse } from "bereach/models/operations";

let value: GetCampaignResponse = {
  success: true,
  campaign: {
    id: "<id>",
    name: "<value>",
    description: null,
    context: "<value>",
    type: "<value>",
    status: "<value>",
    totalContacts: 791538,
    createdAt: "1728257891883",
    updatedAt: "1735653126497",
  },
  creditsUsed: 899575,
  retryAfter: 448071,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `campaign`                                                                         | [operations.GetCampaignCampaign](../../models/operations/get-campaign-campaign.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |