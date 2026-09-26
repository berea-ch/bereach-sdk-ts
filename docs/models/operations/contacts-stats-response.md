# ContactsStatsResponse

Contact statistics

## Example Usage

```typescript
import { ContactsStatsResponse } from "bereach/models/operations";

let value: ContactsStatsResponse = {
  success: true,
  funnel: {
    contact: 384874,
    lead: 875424,
    qualified: 451462,
    rejected: 127820,
  },
  bySource: {
    "key": 381489,
    "key1": 444,
  },
  bySourceAngle: {
    "key": {
      total: 215492,
      contact: 943075,
      lead: 491122,
      qualified: 912365,
      rejected: 467067,
    },
  },
  byCampaign: {},
  daily: [],
  creditsUsed: 162543,
  retryAfter: 80979,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `funnel`                                                                                                                                  | [operations.Funnel](../../models/operations/funnel.md)                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `bySource`                                                                                                                                | Record<string, *number*>                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `bySourceAngle`                                                                                                                           | Record<string, [operations.BySourceAngle](../../models/operations/by-source-angle.md)>                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `byCampaign`                                                                                                                              | Record<string, [operations.ByCampaign](../../models/operations/by-campaign.md)>                                                           | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `daily`                                                                                                                                   | [operations.ContactsStatsDaily](../../models/operations/contacts-stats-daily.md)[]                                                        | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsStatsMeta](../../models/operations/contacts-stats-meta.md)                                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |