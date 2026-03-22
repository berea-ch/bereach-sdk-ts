# UpdateCampaignResponse

Campaign updated

## Example Usage

```typescript
import { UpdateCampaignResponse } from "bereach/models/operations";

let value: UpdateCampaignResponse = {
  success: true,
  campaign: {
    id: "<id>",
    name: "<value>",
    description:
      "indeed positively darling consequently reorganisation ouch next yellowish exalt sternly",
    context: "<value>",
    type: "<value>",
    status: "<value>",
    totalContacts: 869396,
    createdAt: "1717533544301",
    updatedAt: "1735687219134",
  },
  creditsUsed: 701815,
  retryAfter: 298520,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `campaign`                                                                               | [operations.UpdateCampaignCampaign](../../models/operations/update-campaign-campaign.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed by this call (always 0 for contacts queries).                           |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before next call of the same type (always 0 for contacts queries).       |