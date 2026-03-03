# GetMyLinkedInProfileEducation

## Example Usage

```typescript
import { GetMyLinkedInProfileEducation } from "bereach/models/operations";

let value: GetMyLinkedInProfileEducation = {
  schoolName: "<value>",
  degreeName: "<value>",
  fieldOfStudy: "<value>",
  schoolUrl: "https://crowded-elevator.name",
  schoolLogo: "<value>",
  startDate: {
    month: 543709,
    year: 178448,
  },
  endDate: {
    month: 688093,
    year: 389422,
  },
};
```

## Fields

| Field                                                                                                                         | Type                                                                                                                          | Required                                                                                                                      | Description                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `schoolName`                                                                                                                  | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `degreeName`                                                                                                                  | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `fieldOfStudy`                                                                                                                | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `schoolUrl`                                                                                                                   | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `schoolLogo`                                                                                                                  | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `startDate`                                                                                                                   | [operations.GetMyLinkedInProfileEducationStartDate](../../models/operations/get-my-linked-in-profile-education-start-date.md) | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `endDate`                                                                                                                     | [operations.GetMyLinkedInProfileEducationEndDate](../../models/operations/get-my-linked-in-profile-education-end-date.md)     | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |