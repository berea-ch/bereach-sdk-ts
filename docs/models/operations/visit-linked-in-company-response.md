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
    "um considerate massage shark forenenst carnival however scar dishearten alert",
  url: "https://able-adrenalin.org",
  websiteUrl: "https://memorable-simple.info",
  industry: "<value>",
  employeeCount: 171.43,
  employeeCountRange: {
    start: 9989.22,
    end: 4665.4,
  },
  headquarter: null,
  logoUrl: "https://admired-conversation.net/",
  coverImageUrl: "https://empty-editor.info",
  followerCount: 6617.24,
  specialities: [
    "<value 1>",
    "<value 2>",
  ],
  tagline: "<value>",
  isVerified: true,
  foundedOn: {
    year: 5814.29,
  },
  phone: "1-253-666-2427 x11142",
  callToAction: null,
  hashtags: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  affiliatedCompanies: [],
  similarCompanies: [
    {
      id: "<id>",
      universalName: "<value>",
      name: "<value>",
      url: "https://mad-hydrant.info",
      logoUrl: "https://shadowy-midwife.biz/",
      followerCount: 1753.43,
      industry: "<value>",
    },
  ],
  creditsUsed: 172791,
  retryAfter: 815696,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | LinkedIn numeric company ID                                                          |
| `universalName`                                                                      | *string*                                                                             | :heavy_check_mark:                                                                   | Company URL slug                                                                     |
| `name`                                                                               | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `description`                                                                        | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `url`                                                                                | *string*                                                                             | :heavy_check_mark:                                                                   | LinkedIn company page URL                                                            |
| `websiteUrl`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | External website URL                                                                 |
| `industry`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `employeeCount`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | Exact employee count on LinkedIn                                                     |
| `employeeCountRange`                                                                 | [operations.EmployeeCountRange](../../models/operations/employee-count-range.md)     | :heavy_check_mark:                                                                   | Employee count range                                                                 |
| `headquarter`                                                                        | [operations.Headquarter](../../models/operations/headquarter.md)                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `logoUrl`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `coverImageUrl`                                                                      | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `followerCount`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `specialities`                                                                       | *string*[]                                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `tagline`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `isVerified`                                                                         | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `foundedOn`                                                                          | [operations.FoundedOn](../../models/operations/founded-on.md)                        | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `phone`                                                                              | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `callToAction`                                                                       | [operations.CallToAction](../../models/operations/call-to-action.md)                 | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hashtags`                                                                           | *string*[]                                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `affiliatedCompanies`                                                                | [operations.AffiliatedCompany](../../models/operations/affiliated-company.md)[]      | :heavy_check_mark:                                                                   | Showcase / affiliated pages                                                          |
| `similarCompanies`                                                                   | [operations.SimilarCompany](../../models/operations/similar-company.md)[]            | :heavy_check_mark:                                                                   | Similar companies suggested by LinkedIn                                              |
| `workplacePolicy`                                                                    | [operations.WorkplacePolicy](../../models/operations/workplace-policy.md)            | :heavy_minus_sign:                                                                   | Workplace policy (only present when includeWorkplacePolicy=true)                     |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |