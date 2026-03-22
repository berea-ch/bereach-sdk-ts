# CreateCampaignResponse

Campaign created

## Example Usage

```typescript
import { CreateCampaignResponse } from "bereach/models/operations";

let value: CreateCampaignResponse = {
  success: true,
  campaign: {
    id: "<id>",
    name: "<value>",
    description: "bah while pish scale beyond",
    context: "<value>",
    type: "<value>",
    status: "<value>",
    totalContacts: 43656,
    createdAt: "1719927440645",
    updatedAt: "1735678842584",
  },
  creditsUsed: 266957,
  retryAfter: 278870,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `campaign`                                                                               | [operations.CreateCampaignCampaign](../../models/operations/create-campaign-campaign.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed by this call (always 0 for contacts queries).                           |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before next call of the same type (always 0 for contacts queries).       |