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
      nextResetDaily: new Date("2026-11-25T05:18:15.375Z"),
      nextResetWeekly: new Date("2024-08-04T01:46:21.568Z"),
    },
    message: {
      daily: {
        current: 442686,
        limit: 567882,
        remaining: 669069,
      },
      weekly: null,
      minIntervalSeconds: 405884,
      nextResetDaily: new Date("2024-11-28T05:15:02.669Z"),
      nextResetWeekly: new Date("2025-03-22T02:27:07.575Z"),
    },
    profileVisit: {
      daily: {
        current: 195167,
        limit: 586077,
        remaining: 957879,
      },
      weekly: {
        current: 293170,
        limit: 692882,
        remaining: 96344,
      },
      minIntervalSeconds: 984471,
      nextResetDaily: new Date("2024-09-08T18:18:38.386Z"),
      nextResetWeekly: new Date("2024-06-30T16:38:20.025Z"),
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
      minIntervalSeconds: 715944,
      nextResetDaily: new Date("2024-06-15T02:49:32.724Z"),
      nextResetWeekly: new Date("2026-02-12T12:54:07.747Z"),
    },
  },
  creditsUsed: 114833,
  retryAfter: 792378,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `multiplier`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Workspace limit multiplier applied to all base limits (default 1.0)                  |
| `limits`                                                                             | [operations.Limits](../../models/operations/limits.md)                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |