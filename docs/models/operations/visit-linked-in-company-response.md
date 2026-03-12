# VisitLinkedInCompanyResponse

Company profile data

## Example Usage

```typescript
import { VisitLinkedInCompanyResponse } from "bereach/models/operations";

let value: VisitLinkedInCompanyResponse = {
  success: true,
  id: "<id>",
  universalName: "<value>",
  name: "<value>",
  description:
    "aged webbed athwart dependent starboard topsail unexpectedly store elegant",
  url: "https://thorough-rust.org/",
  websiteUrl: "https://odd-aircraft.name",
  industry: null,
  employeeCount: null,
  employeeCountRange: {
    start: 3075.6,
    end: 5097.96,
  },
  headquarter: {
    country: "Maldives",
    geographicArea: "<value>",
    city: null,
    postalCode: "34071-0171",
    line1: "<value>",
    line2: "<value>",
  },
  logoUrl: "https://miserable-petal.name/",
  coverImageUrl: "https://made-up-mom.info/",
  followerCount: 296.09,
  specialities: [
    "<value 1>",
    "<value 2>",
  ],
  tagline: "<value>",
  isVerified: false,
  foundedOn: {
    year: 6783.75,
  },
  phone: "1-471-314-2080 x625",
  callToAction: {
    type: "<value>",
    url: "https://left-corral.info/",
  },
  hashtags: [
    "<value 1>",
    "<value 2>",
  ],
  affiliatedCompanies: [
    {
      id: "<id>",
      universalName: "<value>",
      name: "<value>",
      url: "https://defensive-dead.biz",
      logoUrl: "https://low-captain.net/",
      followerCount: 9974.6,
      industry: "<value>",
    },
  ],
  similarCompanies: [],
  workplacePolicy: {
    title: "<value>",
    description: "but inasmuch meanwhile during",
    timeAtOnsite: "<value>",
    benefits: [
      "<value 1>",
      "<value 2>",
    ],
  },
  creditsUsed: 937996,
  retryAfter: 919883,
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                    | *true*                                                                                                       | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `id`                                                                                                         | *string*                                                                                                     | :heavy_check_mark:                                                                                           | LinkedIn numeric company ID                                                                                  |
| `universalName`                                                                                              | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Company URL slug                                                                                             |
| `name`                                                                                                       | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `description`                                                                                                | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `url`                                                                                                        | *string*                                                                                                     | :heavy_check_mark:                                                                                           | LinkedIn company page URL                                                                                    |
| `websiteUrl`                                                                                                 | *string*                                                                                                     | :heavy_check_mark:                                                                                           | External website URL                                                                                         |
| `industry`                                                                                                   | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `employeeCount`                                                                                              | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Exact employee count on LinkedIn                                                                             |
| `employeeCountRange`                                                                                         | [operations.EmployeeCountRange](../../models/operations/employee-count-range.md)                             | :heavy_check_mark:                                                                                           | Employee count range                                                                                         |
| `headquarter`                                                                                                | [operations.VisitLinkedInCompanyHeadquarter](../../models/operations/visit-linked-in-company-headquarter.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `logoUrl`                                                                                                    | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `coverImageUrl`                                                                                              | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `followerCount`                                                                                              | *number*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `specialities`                                                                                               | *string*[]                                                                                                   | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `tagline`                                                                                                    | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `isVerified`                                                                                                 | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `foundedOn`                                                                                                  | [operations.VisitLinkedInCompanyFoundedOn](../../models/operations/visit-linked-in-company-founded-on.md)    | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `phone`                                                                                                      | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `callToAction`                                                                                               | [operations.CallToAction](../../models/operations/call-to-action.md)                                         | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `hashtags`                                                                                                   | *string*[]                                                                                                   | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `affiliatedCompanies`                                                                                        | [operations.AffiliatedCompany](../../models/operations/affiliated-company.md)[]                              | :heavy_check_mark:                                                                                           | Showcase / affiliated pages                                                                                  |
| `similarCompanies`                                                                                           | [operations.SimilarCompany](../../models/operations/similar-company.md)[]                                    | :heavy_check_mark:                                                                                           | Similar companies suggested by LinkedIn                                                                      |
| `workplacePolicy`                                                                                            | [operations.WorkplacePolicy](../../models/operations/workplace-policy.md)                                    | :heavy_check_mark:                                                                                           | Workplace policy (null when includeWorkplacePolicy is false or data unavailable)                             |
| `creditsUsed`                                                                                                | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                         |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                         |