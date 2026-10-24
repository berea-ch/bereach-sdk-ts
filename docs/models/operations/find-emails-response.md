# FindEmailsResponse

One row per person, with the email credits this call spent

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
  emailCreditsUsed: 452290,
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `success`                                                                      | *true*                                                                         | :heavy_check_mark:                                                             | N/A                                                                            |
| `people`                                                                       | [operations.FindEmailsPerson](../../models/operations/find-emails-person.md)[] | :heavy_check_mark:                                                             | N/A                                                                            |
| `found`                                                                        | *number*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `emailCreditsUsed`                                                             | *number*                                                                       | :heavy_check_mark:                                                             | Email credits this call spent: one per email found now.                        |
| `buyCreditsUrl`                                                                | *string*                                                                       | :heavy_minus_sign:                                                             | Where to buy a pack of email credits, when they ran out.                       |
| `note`                                                                         | *string*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |