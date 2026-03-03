# GetMyLimitsResponse

Rate limit status for all action types

## Example Usage

```typescript
import { GetMyLimitsResponse } from "bereach/models/operations";

let value: GetMyLimitsResponse = {
  success: true,
  multiplier: 1063.89,
  limits: {
    connectionRequest: {
      daily: {
        current: 343739,
        limit: 632124,
        remaining: 392167,
      },
      weekly: {
        current: 53997,
        limit: 183170,
        remaining: 905903,
      },
      minIntervalSeconds: 407168,
      nextResetDaily: new Date("2025-01-28T12:20:37.701Z"),
      nextResetWeekly: new Date("2026-06-21T23:56:45.599Z"),
    },
    message: {
      daily: {
        current: 278613,
        limit: 537376,
        remaining: 221249,
      },
      weekly: {
        current: 252572,
        limit: 664834,
        remaining: 626371,
      },
      minIntervalSeconds: 748795,
      nextResetDaily: new Date("2026-11-25T05:18:15.375Z"),
      nextResetWeekly: new Date("2024-08-04T01:46:21.568Z"),
    },
    profileVisit: {
      daily: {
        current: 41832,
        limit: 508530,
        remaining: 293170,
      },
      weekly: {
        current: 96344,
        limit: 944086,
        remaining: 791982,
      },
      minIntervalSeconds: 15601,
      nextResetDaily: new Date("2025-03-20T20:21:59.635Z"),
      nextResetWeekly: new Date("2024-11-28T05:15:02.669Z"),
    },
    scraping: {
      daily: {
        current: 761224,
        limit: 601148,
        remaining: 137081,
      },
      weekly: {
        current: 407027,
        limit: 410694,
        remaining: 195167,
      },
      minIntervalSeconds: 586077,
      nextResetDaily: new Date("2026-11-15T20:01:53.215Z"),
      nextResetWeekly: new Date("2026-12-14T23:31:15.376Z"),
    },
  },
  creditsUsed: 901544,
  retryAfter: 656743,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `multiplier`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Workspace limit multiplier applied to all base limits (default 1.0)                  |
| `limits`                                                                             | [operations.Limits](../../models/operations/limits.md)                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |