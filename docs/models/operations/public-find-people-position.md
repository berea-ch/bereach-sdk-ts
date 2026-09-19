# PublicFindPeoplePosition

## Example Usage

```typescript
import { PublicFindPeoplePosition } from "bereach/models/operations";

let value: PublicFindPeoplePosition = {
  companyName: "Padberg - Donnelly",
  title: "<value>",
  companyUrl: "https://rural-birdbath.info",
  startDate: {
    year: 3975.33,
  },
  endDate: {
    year: 2655.3,
  },
  isCurrent: true,
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                                     | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `title`                                                                                                           | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `companyUrl`                                                                                                      | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `startDate`                                                                                                       | [operations.PublicFindPeoplePositionStartDate](../../models/operations/public-find-people-position-start-date.md) | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `endDate`                                                                                                         | [operations.PublicFindPeoplePositionEndDate](../../models/operations/public-find-people-position-end-date.md)     | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `isCurrent`                                                                                                       | *boolean*                                                                                                         | :heavy_check_mark:                                                                                                | N/A                                                                                                               |