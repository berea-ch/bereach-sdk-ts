# ContactEmployer

The company whose record was read for this person, when a size band or a company check asked for it.

## Example Usage

```typescript
import { ContactEmployer } from "bereach/models/operations";

let value: ContactEmployer = {
  name: "<value>",
  employees: 1737.59,
  industry: "<value>",
  hq: {
    city: null,
    postcode: "06998-9737",
    country: "Serbia",
  },
  linkedinUrl: "https://defensive-promise.biz/",
  website: null,
  readAt: "<value>",
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `name`                                                        | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `employees`                                                   | *number*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `industry`                                                    | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `hq`                                                          | [operations.ContactHq](../../models/operations/contact-hq.md) | :heavy_check_mark:                                            | N/A                                                           |
| `linkedinUrl`                                                 | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `website`                                                     | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `readAt`                                                      | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |