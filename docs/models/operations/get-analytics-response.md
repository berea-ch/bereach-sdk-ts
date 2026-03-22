# GetAnalyticsResponse

Company page overview analytics

## Example Usage

```typescript
import { GetAnalyticsResponse } from "bereach/models/operations";

let value: GetAnalyticsResponse = {
  success: true,
  analytics: {
    name: "<value>",
    universalName: "<value>",
    followerCount: null,
    employeeCount: 385275,
    visitorsInPastMonthCount: 570073,
    isActive: false,
    foundedOn: {
      year: 1528.42,
    },
    headquarter: {
      city: "Fort Orvalview",
      country: "Oman",
    },
    description: "soon over far beyond pocket-watch opposite suckle woot gosh",
    tagline: "<value>",
    websiteUrl: "https://utilized-marketplace.info/",
    organizationType: "<value>",
    specialities: [
      "<value 1>",
      "<value 2>",
    ],
    industryUrns: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  creditsUsed: 406545,
  retryAfter: 165975,
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `success`                                                                              | *true*                                                                                 | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `analytics`                                                                            | [operations.GetAnalyticsAnalytics](../../models/operations/get-analytics-analytics.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `creditsUsed`                                                                          | *number*                                                                               | :heavy_check_mark:                                                                     | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).   |
| `retryAfter`                                                                           | *number*                                                                               | :heavy_check_mark:                                                                     | Seconds to wait before making another call of the same type. 0 means no wait needed.   |