# RefreshEducation

## Example Usage

```typescript
import { RefreshEducation } from "bereach/models/operations";

let value: RefreshEducation = {
  schoolName: "<value>",
  degreeName: "<value>",
  fieldOfStudy: null,
  schoolUrl: "https://excitable-habit.biz/",
  schoolLogo: "<value>",
  startDate: {
    month: 434203,
    year: 868462,
  },
  endDate: {
    month: 804039,
    year: 714104,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `schoolName`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `degreeName`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `fieldOfStudy`                                                                                  | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `schoolUrl`                                                                                     | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `schoolLogo`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `startDate`                                                                                     | [operations.RefreshEducationStartDate](../../models/operations/refresh-education-start-date.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `endDate`                                                                                       | [operations.RefreshEducationEndDate](../../models/operations/refresh-education-end-date.md)     | :heavy_check_mark:                                                                              | N/A                                                                                             |