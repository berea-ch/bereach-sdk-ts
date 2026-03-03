# GetMyLinkedInProfilePosition

## Example Usage

```typescript
import { GetMyLinkedInProfilePosition } from "bereach/models/operations";

let value: GetMyLinkedInProfilePosition = {
  companyName: "Harris Group",
  title: "<value>",
  companyUrl: "https://cavernous-bathhouse.biz",
  companyLogo: "<value>",
  startDate: {
    month: 190954,
    year: 21755,
  },
  endDate: {
    month: 51829,
    year: 203236,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                                                       | Type                                                                                                                        | Required                                                                                                                    | Description                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                                               | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `title`                                                                                                                     | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `companyUrl`                                                                                                                | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `companyLogo`                                                                                                               | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `startDate`                                                                                                                 | [operations.GetMyLinkedInProfilePositionStartDate](../../models/operations/get-my-linked-in-profile-position-start-date.md) | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `endDate`                                                                                                                   | [operations.GetMyLinkedInProfilePositionEndDate](../../models/operations/get-my-linked-in-profile-position-end-date.md)     | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `isCurrent`                                                                                                                 | *boolean*                                                                                                                   | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |