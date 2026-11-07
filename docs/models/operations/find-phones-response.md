# FindPhonesResponse

One row per person, with what this call spent

## Example Usage

```typescript
import { FindPhonesResponse } from "bereach/models/operations";

let value: FindPhonesResponse = {
  success: true,
  people: [
    {
      contactId: "<id>",
      profileUrl: "https://insecure-scaffold.biz",
      name: "<value>",
      phone: "(928) 318-1171 x33202",
      lineType: "<value>",
      countryCode: "NA",
      status: "found",
      saved: false,
    },
  ],
  found: 979675,
  creditsUsed: 271042,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `people`                                                                                                                             | [operations.FindPhonesPerson](../../models/operations/find-phones-person.md)[]                                                       | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `found`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.FindPhonesSpent](../../models/operations/find-phones-spent.md)                                                           | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `topUpUrl`                                                                                                                           | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Where money is added, when nothing was left to spend.                                                                                |
| `note`                                                                                                                               | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | N/A                                                                                                                                  |