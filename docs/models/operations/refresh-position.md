# RefreshPosition

## Example Usage

```typescript
import { RefreshPosition } from "bereach/models/operations";

let value: RefreshPosition = {
  companyName: "Hayes, Fritsch and Auer",
  title: "<value>",
  companyUrl: "https://great-wear.org/",
  companyLogo: "<value>",
  startDate: {
    month: 387995,
    year: 279712,
  },
  endDate: {
    month: 352134,
    year: 175919,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `companyName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `companyUrl`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `companyLogo`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `startDate`                                                                                   | [operations.RefreshPositionStartDate](../../models/operations/refresh-position-start-date.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `endDate`                                                                                     | [operations.RefreshPositionEndDate](../../models/operations/refresh-position-end-date.md)     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `isCurrent`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |