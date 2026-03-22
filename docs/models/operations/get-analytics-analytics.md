# GetAnalyticsAnalytics

## Example Usage

```typescript
import { GetAnalyticsAnalytics } from "bereach/models/operations";

let value: GetAnalyticsAnalytics = {
  name: "<value>",
  universalName: "<value>",
  followerCount: 343526,
  employeeCount: 590614,
  visitorsInPastMonthCount: 49513,
  isActive: true,
  foundedOn: {
    year: 1528.42,
  },
  headquarter: {
    city: "Fort Orvalview",
    country: "Oman",
  },
  description: "usefully hungry orderly boo",
  tagline: "<value>",
  websiteUrl: "https://awful-stitcher.org",
  organizationType: "<value>",
  specialities: [
    "<value 1>",
  ],
  industryUrns: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `name`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `universalName`                                                                            | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `followerCount`                                                                            | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `employeeCount`                                                                            | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `visitorsInPastMonthCount`                                                                 | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `isActive`                                                                                 | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `foundedOn`                                                                                | [operations.GetAnalyticsFoundedOn](../../models/operations/get-analytics-founded-on.md)    | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `headquarter`                                                                              | [operations.GetAnalyticsHeadquarter](../../models/operations/get-analytics-headquarter.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `description`                                                                              | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `tagline`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `websiteUrl`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `organizationType`                                                                         | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `specialities`                                                                             | *string*[]                                                                                 | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `industryUrns`                                                                             | *string*[]                                                                                 | :heavy_check_mark:                                                                         | N/A                                                                                        |