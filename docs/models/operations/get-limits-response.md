# GetLimitsResponse

Rate limit status for all action types

## Example Usage

```typescript
import { GetLimitsResponse } from "bereach/models/operations";

let value: GetLimitsResponse = {
  success: true,
  multiplier: 6690.82,
  limits: {
    connectionRequest: {
      uncapped: false,
      daily: {
        current: 392167,
        limit: 620172,
        remaining: 53997,
      },
      weekly: {
        current: 905903,
        limit: 617573,
        remaining: 804803,
      },
      minIntervalSeconds: 376830,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    message: {
      uncapped: false,
      daily: {
        current: 567882,
        limit: 669069,
        remaining: 636753,
      },
      weekly: {
        current: 534020,
        limit: 472297,
        remaining: 863521,
      },
      minIntervalSeconds: 197147,
      nextResetDaily: "<value>",
      nextResetWeekly: null,
    },
    profileVisit: {
      uncapped: true,
      daily: {
        current: 293170,
        limit: 692882,
        remaining: 96344,
      },
      weekly: {
        current: 791982,
        limit: 483792,
        remaining: 394394,
      },
      minIntervalSeconds: 558979,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    scraping: {
      uncapped: true,
      daily: {
        current: 137081,
        limit: 85944,
        remaining: 814423,
      },
      weekly: {
        current: 285349,
        limit: 899452,
        remaining: 708085,
      },
      minIntervalSeconds: 992300,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
  },
  creditsUsed: 114833,
  retryAfter: 792378,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `multiplier`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Workspace limit multiplier applied to all base limits (default 1.0)                                                                       |
| `limits`                                                                                                                                  | [operations.Limits](../../models/operations/limits.md)                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetLimitsMeta](../../models/operations/get-limits-meta.md)                                                                    | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |