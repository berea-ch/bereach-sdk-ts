# GetProfileEducation

## Example Usage

```typescript
import { GetProfileEducation } from "bereach/models/operations";

let value: GetProfileEducation = {
  schoolName: "<value>",
  degreeName: "<value>",
  fieldOfStudy: "<value>",
  schoolUrl: "https://delectable-tail.org/",
  schoolLogo: "<value>",
  startDate: null,
  endDate: {
    month: 335198,
    year: 368323,
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `schoolName`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `degreeName`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `fieldOfStudy`                                                                                         | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `schoolUrl`                                                                                            | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `schoolLogo`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `startDate`                                                                                            | [operations.GetProfileEducationStartDate](../../models/operations/get-profile-education-start-date.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `endDate`                                                                                              | [operations.GetProfileEducationEndDate](../../models/operations/get-profile-education-end-date.md)     | :heavy_check_mark:                                                                                     | N/A                                                                                                    |