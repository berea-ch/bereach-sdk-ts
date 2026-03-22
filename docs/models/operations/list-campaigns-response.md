# ListCampaignsResponse

Campaigns list

## Example Usage

```typescript
import { ListCampaignsResponse } from "bereach/models/operations";

let value: ListCampaignsResponse = {
  success: true,
  campaigns: [],
  pagination: {
    limit: 353920,
    offset: 445446,
    total: 922855,
  },
  creditsUsed: 308582,
  retryAfter: 862157,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `success`                                                                                  | *true*                                                                                     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `campaigns`                                                                                | [operations.ListCampaignsCampaign](../../models/operations/list-campaigns-campaign.md)[]   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `pagination`                                                                               | [operations.ListCampaignsPagination](../../models/operations/list-campaigns-pagination.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `creditsUsed`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | Credits consumed by this call (always 0 for contacts queries).                             |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before next call of the same type (always 0 for contacts queries).         |