# Analytics

## Example Usage

```typescript
import { Analytics } from "bereach/models/operations";

let value: Analytics = {
  name: "<value>",
  universalName: "<value>",
  followerCount: 36533,
  employeeCount: 87161,
  visitorsInPastMonthCount: 36309,
  isActive: true,
  foundedOn: {
    year: 8339.48,
  },
  headquarter: {
    city: "Hammond",
    country: "Sri Lanka",
  },
  description: null,
  tagline: "<value>",
  websiteUrl: "https://imaginary-peony.net",
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
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `name`                                                                                                             | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `universalName`                                                                                                    | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `followerCount`                                                                                                    | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `employeeCount`                                                                                                    | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `visitorsInPastMonthCount`                                                                                         | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `isActive`                                                                                                         | *boolean*                                                                                                          | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `foundedOn`                                                                                                        | [operations.GetCompanyPageAnalyticsFoundedOn](../../models/operations/get-company-page-analytics-founded-on.md)    | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `headquarter`                                                                                                      | [operations.GetCompanyPageAnalyticsHeadquarter](../../models/operations/get-company-page-analytics-headquarter.md) | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `description`                                                                                                      | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `tagline`                                                                                                          | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `websiteUrl`                                                                                                       | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `organizationType`                                                                                                 | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `specialities`                                                                                                     | *string*[]                                                                                                         | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `industryUrns`                                                                                                     | *string*[]                                                                                                         | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |