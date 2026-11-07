# FindEmailsResponse

One row per person, with what this call spent

## Example Usage

```typescript
import { FindEmailsResponse } from "bereach/models/operations";

let value: FindEmailsResponse = {
  success: true,
  people: [
    {
      contactId: "<id>",
      profileUrl: "https://rowdy-underneath.biz",
      name: "<value>",
      email: "Katelyn.Schoen@gmail.com",
      verified: false,
      status: "not_looked_up",
      saved: false,
    },
  ],
  found: 438290,
  creditsUsed: 452290,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `people`                                                                                                                             | [operations.FindEmailsPerson](../../models/operations/find-emails-person.md)[]                                                       | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `found`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.FindEmailsSpent](../../models/operations/find-emails-spent.md)                                                           | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `topUpUrl`                                                                                                                           | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Where money is added, when nothing was left to spend.                                                                                |
| `note`                                                                                                                               | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | N/A                                                                                                                                  |