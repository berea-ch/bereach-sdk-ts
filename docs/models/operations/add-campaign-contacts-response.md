# AddCampaignContactsResponse

Contacts added

## Example Usage

```typescript
import { AddCampaignContactsResponse } from "bereach/models/operations";

let value: AddCampaignContactsResponse = {
  success: true,
  results: {
    created: 545761,
    skipped: 298616,
    errors: [],
  },
  creditsUsed: 875503,
  retryAfter: 443570,
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `success`                                                                                         | *true*                                                                                            | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `results`                                                                                         | [operations.AddCampaignContactsResults](../../models/operations/add-campaign-contacts-results.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `creditsUsed`                                                                                     | *number*                                                                                          | :heavy_check_mark:                                                                                | Credits consumed by this call (always 0 for contacts queries).                                    |
| `retryAfter`                                                                                      | *number*                                                                                          | :heavy_check_mark:                                                                                | Seconds to wait before next call of the same type (always 0 for contacts queries).                |