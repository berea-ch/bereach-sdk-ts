# ContactsListCampaignsResponse

Campaigns list

## Example Usage

```typescript
import { ContactsListCampaignsResponse } from "bereach/models/operations";

let value: ContactsListCampaignsResponse = {
  success: true,
  campaigns: [],
  pagination: {
    limit: 46073,
    offset: 486417,
    total: 181531,
  },
  creditsUsed: 368013,
  retryAfter: 442399,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `campaigns`                                                                                                                       | [operations.ContactsListCampaignsCampaign](../../models/operations/contacts-list-campaigns-campaign.md)[]                         | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `pagination`                                                                                                                      | [operations.ContactsListCampaignsPagination](../../models/operations/contacts-list-campaigns-pagination.md)                       | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |