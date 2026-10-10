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

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `campaigns`                                                                                                                               | [operations.ContactsListCampaignsCampaign](../../models/operations/contacts-list-campaigns-campaign.md)[]                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `pagination`                                                                                                                              | [operations.ContactsListCampaignsPagination](../../models/operations/contacts-list-campaigns-pagination.md)                               | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsListCampaignsMeta](../../models/operations/contacts-list-campaigns-meta.md)                                           | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |