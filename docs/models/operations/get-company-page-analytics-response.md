# GetCompanyPageAnalyticsResponse

Company page overview analytics

## Example Usage

```typescript
import { GetCompanyPageAnalyticsResponse } from "bereach/models/operations";

let value: GetCompanyPageAnalyticsResponse = {
  success: true,
  analytics: {
    name: "<value>",
    universalName: "<value>",
    followerCount: 238618,
    employeeCount: 625659,
    visitorsInPastMonthCount: 147831,
    isActive: true,
    foundedOn: {
      year: 8339.48,
    },
    headquarter: {
      city: "Hammond",
      country: "Sri Lanka",
    },
    description: "and denitrify integer breed slap gerbil",
    tagline: "<value>",
    websiteUrl: "https://afraid-scenario.org",
    organizationType: "<value>",
    specialities: [
      "<value 1>",
    ],
    industryUrns: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  creditsUsed: 157988,
  retryAfter: 447526,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `analytics`                                                                          | [operations.Analytics](../../models/operations/analytics.md)                         | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |