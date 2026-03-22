# GetPostAnalyticsResponse

Post analytics

## Example Usage

```typescript
import { GetPostAnalyticsResponse } from "bereach/models/operations";

let value: GetPostAnalyticsResponse = {
  success: true,
  analytics: {
    reactions: 899963,
    comments: 165007,
    postUrn: "<value>",
  },
  creditsUsed: 457545,
  retryAfter: 814314,
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `success`                                                                                       | *true*                                                                                          | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `analytics`                                                                                     | [operations.GetPostAnalyticsAnalytics](../../models/operations/get-post-analytics-analytics.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `creditsUsed`                                                                                   | *number*                                                                                        | :heavy_check_mark:                                                                              | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).            |
| `retryAfter`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | Seconds to wait before making another call of the same type. 0 means no wait needed.            |