# GetLinkedInFollowerAnalyticsResponse

Follower analytics

## Example Usage

```typescript
import { GetLinkedInFollowerAnalyticsResponse } from "bereach/models/operations";

let value: GetLinkedInFollowerAnalyticsResponse = {
  success: true,
  analytics: "<value>",
  creditsUsed: 103279,
  retryAfter: 456131,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `analytics`                                                                          | *any*                                                                                | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |