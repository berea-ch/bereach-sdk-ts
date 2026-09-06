# CompanyPageAnalyticsResponse

Company page overview analytics

## Example Usage

```typescript
import { CompanyPageAnalyticsResponse } from "bereach/models/operations";

let value: CompanyPageAnalyticsResponse = {
  success: true,
  analytics: {
    name: "<value>",
    universalName: "<value>",
    followerCount: 831813,
    employeeCount: 760364,
    visitorsInPastMonthCount: 664515,
    isActive: true,
    foundedOn: {
      year: 8339.48,
    },
    headquarter: {
      city: "Hammond",
      country: "Sri Lanka",
    },
    description: "underneath instead unless ride gosh gadzooks yippee than",
    tagline: "<value>",
    websiteUrl: "https://altruistic-transparency.info",
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
  creditsUsed: 161637,
  retryAfter: 162637,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `analytics`                                                                                                                               | [operations.Analytics](../../models/operations/analytics.md)                                                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CompanyPageAnalyticsMeta](../../models/operations/company-page-analytics-meta.md)                                             | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |