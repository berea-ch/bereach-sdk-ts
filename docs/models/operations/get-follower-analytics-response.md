# GetFollowerAnalyticsResponse

Follower analytics

## Example Usage

```typescript
import { GetFollowerAnalyticsResponse } from "bereach/models/operations";

let value: GetFollowerAnalyticsResponse = {
  success: true,
  analytics: {
    count: 723063,
  },
  creditsUsed: 431370,
  retryAfter: 336255,
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `success`                                                                                               | *true*                                                                                                  | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `analytics`                                                                                             | [operations.GetFollowerAnalyticsAnalytics](../../models/operations/get-follower-analytics-analytics.md) | :heavy_check_mark:                                                                                      | Follower count and optional growth/demographics data from LinkedIn                                      |
| `creditsUsed`                                                                                           | *number*                                                                                                | :heavy_check_mark:                                                                                      | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                    |
| `retryAfter`                                                                                            | *number*                                                                                                | :heavy_check_mark:                                                                                      | Seconds to wait before making another call of the same type. 0 means no wait needed.                    |