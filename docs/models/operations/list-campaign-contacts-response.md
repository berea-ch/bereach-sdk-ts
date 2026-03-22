# ListCampaignContactsResponse

Campaign contacts

## Example Usage

```typescript
import { ListCampaignContactsResponse } from "bereach/models/operations";

let value: ListCampaignContactsResponse = {
  success: true,
  contacts: [],
  pagination: {
    limit: 728166,
    offset: 953038,
    total: 21029,
  },
  creditsUsed: 551730,
  retryAfter: 58897,
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                 | *true*                                                                                                    | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `contacts`                                                                                                | [operations.ListCampaignContactsContact](../../models/operations/list-campaign-contacts-contact.md)[]     | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `pagination`                                                                                              | [operations.ListCampaignContactsPagination](../../models/operations/list-campaign-contacts-pagination.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `creditsUsed`                                                                                             | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Credits consumed by this call (always 0 for contacts queries).                                            |
| `retryAfter`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Seconds to wait before next call of the same type (always 0 for contacts queries).                        |