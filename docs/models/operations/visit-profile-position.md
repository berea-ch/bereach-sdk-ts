# VisitProfilePosition

## Example Usage

```typescript
import { VisitProfilePosition } from "bereach/models/operations";

let value: VisitProfilePosition = {
  companyName: "Upton Group",
  title: "<value>",
  description: "hubris sleepily scarily swing pfft up around tiny",
  companyUrl: "https://juvenile-ferret.name/",
  companyLogo: "<value>",
  companyDescription: "<value>",
  startDate: {
    month: 349967,
    year: 495764,
  },
  endDate: {
    month: 683967,
    year: 129783,
  },
  isCurrent: true,
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                            | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `title`                                                                                                  | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `description`                                                                                            | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Position description / responsibilities text                                                             |
| `companyUrl`                                                                                             | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `companyLogo`                                                                                            | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `companyDescription`                                                                                     | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Short description of the company (from LinkedIn company page)                                            |
| `startDate`                                                                                              | [operations.VisitProfilePositionStartDate](../../models/operations/visit-profile-position-start-date.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `endDate`                                                                                                | [operations.VisitProfilePositionEndDate](../../models/operations/visit-profile-position-end-date.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `isCurrent`                                                                                              | *boolean*                                                                                                | :heavy_check_mark:                                                                                       | N/A                                                                                                      |