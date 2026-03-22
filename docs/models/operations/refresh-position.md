# RefreshPosition

## Example Usage

```typescript
import { RefreshPosition } from "bereach/models/operations";

let value: RefreshPosition = {
  companyName: "Hayes, Fritsch and Auer",
  title: "<value>",
  description: "joyously before bid",
  companyUrl: "https://sturdy-fireplace.name/",
  companyLogo: "<value>",
  companyDescription: "<value>",
  startDate: {
    month: 811924,
    year: 660821,
  },
  endDate: {
    month: 660549,
    year: 488511,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `companyName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Position description / responsibilities text                                                  |
| `companyUrl`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `companyLogo`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `companyDescription`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Short description of the company (from LinkedIn company page)                                 |
| `startDate`                                                                                   | [operations.RefreshPositionStartDate](../../models/operations/refresh-position-start-date.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `endDate`                                                                                     | [operations.RefreshPositionEndDate](../../models/operations/refresh-position-end-date.md)     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `isCurrent`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |