# GetProfilePosition

## Example Usage

```typescript
import { GetProfilePosition } from "bereach/models/operations";

let value: GetProfilePosition = {
  companyName: "Homenick, Heaney and Abernathy",
  title: "<value>",
  description: "whirlwind outflank astride descriptive",
  companyUrl: "https://apt-adaptation.info",
  companyLogo: "<value>",
  companyDescription: "<value>",
  startDate: {
    month: 706031,
    year: 105182,
  },
  endDate: {
    month: 145193,
    year: 571552,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `title`                                                                                              | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `description`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | Position description / responsibilities text                                                         |
| `companyUrl`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `companyLogo`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `companyDescription`                                                                                 | *string*                                                                                             | :heavy_check_mark:                                                                                   | Short description of the company (from LinkedIn company page)                                        |
| `startDate`                                                                                          | [operations.GetProfilePositionStartDate](../../models/operations/get-profile-position-start-date.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `endDate`                                                                                            | [operations.GetProfilePositionEndDate](../../models/operations/get-profile-position-end-date.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `isCurrent`                                                                                          | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |