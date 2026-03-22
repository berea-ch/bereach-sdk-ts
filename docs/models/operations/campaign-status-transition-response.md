# CampaignStatusTransitionResponse

Status updated

## Example Usage

```typescript
import { CampaignStatusTransitionResponse } from "bereach/models/operations";

let value: CampaignStatusTransitionResponse = {
  success: true,
  campaign: {
    id: "<id>",
    name: "<value>",
    description: "boo naturally where paintwork",
    context: "<value>",
    type: "<value>",
    status: "<value>",
    totalContacts: 724112,
    createdAt: "1722769383941",
    updatedAt: "1735627876088",
  },
  creditsUsed: 303867,
  retryAfter: 634165,
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                     | *true*                                                                                                        | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `campaign`                                                                                                    | [operations.CampaignStatusTransitionCampaign](../../models/operations/campaign-status-transition-campaign.md) | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `creditsUsed`                                                                                                 | *number*                                                                                                      | :heavy_check_mark:                                                                                            | Credits consumed by this call (always 0 for contacts queries).                                                |
| `retryAfter`                                                                                                  | *number*                                                                                                      | :heavy_check_mark:                                                                                            | Seconds to wait before next call of the same type (always 0 for contacts queries).                            |