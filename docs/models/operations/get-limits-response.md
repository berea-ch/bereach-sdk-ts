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
      daily: {
        current: 632124,
        limit: 392167,
        remaining: 620172,
      },
      weekly: {
        current: 359046,
        limit: 376830,
        remaining: 823903,
      },
      minIntervalSeconds: 332064,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    message: {
      daily: {
        current: 442686,
        limit: 567882,
        remaining: 669069,
      },
      weekly: {
        current: 830346,
        limit: 534020,
        remaining: 472297,
      },
      minIntervalSeconds: 488543,
      nextResetDaily: null,
      nextResetWeekly: "<value>",
    },
    profileVisit: {
      daily: {
        current: 303119,
        limit: 558979,
        remaining: 407027,
      },
      weekly: {
        current: 293170,
        limit: 692882,
        remaining: 96344,
      },
      minIntervalSeconds: 195167,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    scraping: {
      daily: {
        current: 601148,
        limit: 137081,
        remaining: 85944,
      },
      weekly: {
        current: 890676,
        limit: 285349,
        remaining: 899452,
      },
      minIntervalSeconds: 474427,
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