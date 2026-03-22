# GetContactStatsResponse

Contact statistics

## Example Usage

```typescript
import { GetContactStatsResponse } from "bereach/models/operations";

let value: GetContactStatsResponse = {
  success: true,
  funnel: {
    contact: 344558,
    lead: 407268,
    qualified: 170421,
    approved: 515677,
    rejected: 738566,
  },
  bySource: {
    "key": 901860,
    "key1": 304265,
  },
  bySourceAngle: {},
  byCampaign: {},
  daily: [],
  creditsUsed: 621770,
  retryAfter: 580197,
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `success`                                                                               | *true*                                                                                  | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `funnel`                                                                                | [operations.Funnel](../../models/operations/funnel.md)                                  | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `bySource`                                                                              | Record<string, *number*>                                                                | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `bySourceAngle`                                                                         | Record<string, [operations.BySourceAngle](../../models/operations/by-source-angle.md)>  | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `byCampaign`                                                                            | Record<string, [operations.ByCampaign](../../models/operations/by-campaign.md)>         | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `daily`                                                                                 | [operations.GetContactStatsDaily](../../models/operations/get-contact-stats-daily.md)[] | :heavy_check_mark:                                                                      | N/A                                                                                     |
| `creditsUsed`                                                                           | *number*                                                                                | :heavy_check_mark:                                                                      | Credits consumed by this call (always 0 for contacts queries).                          |
| `retryAfter`                                                                            | *number*                                                                                | :heavy_check_mark:                                                                      | Seconds to wait before next call of the same type (always 0 for contacts queries).      |