# VisitProfileEducation

## Example Usage

```typescript
import { VisitProfileEducation } from "bereach/models/operations";

let value: VisitProfileEducation = {
  schoolName: "<value>",
  degreeName: "<value>",
  fieldOfStudy: "<value>",
  schoolUrl: "https://evil-vista.org",
  schoolLogo: null,
  startDate: {
    month: 243795,
    year: 869513,
  },
  endDate: {
    month: 837292,
    year: 115765,
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `schoolName`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `degreeName`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `fieldOfStudy`                                                                                             | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `schoolUrl`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `schoolLogo`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `startDate`                                                                                                | [operations.VisitProfileEducationStartDate](../../models/operations/visit-profile-education-start-date.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `endDate`                                                                                                  | [operations.VisitProfileEducationEndDate](../../models/operations/visit-profile-education-end-date.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |