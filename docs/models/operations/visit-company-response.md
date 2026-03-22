# VisitCompanyResponse

Company profile data

## Example Usage

```typescript
import { VisitCompanyResponse } from "bereach/models/operations";

let value: VisitCompanyResponse = {
  success: true,
  id: "<id>",
  universalName: "<value>",
  name: "<value>",
  description: "aggravating accentuate trick purple",
  url: "https://prime-netsuke.name",
  websiteUrl: "https://true-chap.name",
  industry: "<value>",
  employeeCount: null,
  employeeCountRange: {
    start: 4226.48,
    end: 6874.57,
  },
  headquarter: {
    country: "Puerto Rico",
    geographicArea: "<value>",
    city: "North Deonteton",
    postalCode: "40090-8165",
    line1: "<value>",
    line2: "<value>",
  },
  logoUrl: "https://squeaky-antelope.biz/",
  coverImageUrl: "https://slight-illusion.net",
  followerCount: 1431.91,
  specialities: [
    "<value 1>",
    "<value 2>",
  ],
  tagline: "<value>",
  isVerified: false,
  foundedOn: {
    year: 9992.22,
  },
  phone: "1-249-752-8464",
  callToAction: {
    type: "<value>",
    url: "https://accomplished-slipper.biz/",
  },
  hashtags: [
    "<value 1>",
  ],
  affiliatedCompanies: [
    {
      id: "<id>",
      universalName: "<value>",
      name: "<value>",
      url: "https://useless-numeric.net",
      logoUrl: "https://electric-husband.info/",
      followerCount: 177.68,
      industry: "<value>",
    },
  ],
  similarCompanies: [],
  workplacePolicy: {
    title: "<value>",
    description: "role midst whoa ownership upside-down decent off",
    timeAtOnsite: "<value>",
    benefits: [
      "<value 1>",
    ],
  },
  creditsUsed: 121133,
  retryAfter: 300881,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `success`                                                                                  | *true*                                                                                     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `id`                                                                                       | *string*                                                                                   | :heavy_check_mark:                                                                         | LinkedIn numeric company ID                                                                |
| `universalName`                                                                            | *string*                                                                                   | :heavy_check_mark:                                                                         | Company URL slug                                                                           |
| `name`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `description`                                                                              | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `url`                                                                                      | *string*                                                                                   | :heavy_check_mark:                                                                         | LinkedIn company page URL                                                                  |
| `websiteUrl`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | External website URL                                                                       |
| `industry`                                                                                 | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `employeeCount`                                                                            | *number*                                                                                   | :heavy_check_mark:                                                                         | Exact employee count on LinkedIn                                                           |
| `employeeCountRange`                                                                       | [operations.EmployeeCountRange](../../models/operations/employee-count-range.md)           | :heavy_check_mark:                                                                         | Employee count range                                                                       |
| `headquarter`                                                                              | [operations.VisitCompanyHeadquarter](../../models/operations/visit-company-headquarter.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `logoUrl`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `coverImageUrl`                                                                            | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `followerCount`                                                                            | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `specialities`                                                                             | *string*[]                                                                                 | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `tagline`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `isVerified`                                                                               | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `foundedOn`                                                                                | [operations.VisitCompanyFoundedOn](../../models/operations/visit-company-founded-on.md)    | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `phone`                                                                                    | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `callToAction`                                                                             | [operations.CallToAction](../../models/operations/call-to-action.md)                       | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `hashtags`                                                                                 | *string*[]                                                                                 | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `affiliatedCompanies`                                                                      | [operations.AffiliatedCompany](../../models/operations/affiliated-company.md)[]            | :heavy_check_mark:                                                                         | Showcase / affiliated pages                                                                |
| `similarCompanies`                                                                         | [operations.SimilarCompany](../../models/operations/similar-company.md)[]                  | :heavy_check_mark:                                                                         | Similar companies suggested by LinkedIn                                                    |
| `workplacePolicy`                                                                          | [operations.WorkplacePolicy](../../models/operations/workplace-policy.md)                  | :heavy_check_mark:                                                                         | Workplace policy (null when includeWorkplacePolicy is false or data unavailable)           |
| `creditsUsed`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).       |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before making another call of the same type. 0 means no wait needed.       |