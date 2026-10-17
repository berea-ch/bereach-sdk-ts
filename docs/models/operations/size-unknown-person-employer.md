# SizeUnknownPersonEmployer

The company whose record was read for this person, when a size band or a company check asked for it.

## Example Usage

```typescript
import { SizeUnknownPersonEmployer } from "bereach/models/operations";

let value: SizeUnknownPersonEmployer = {
  name: "<value>",
  employees: null,
  industry: "<value>",
  hq: {
    city: "Port Colefurt",
    postcode: "04203",
    country: "Jamaica",
  },
  linkedinUrl: "https://average-anticodon.biz",
  website: "<value>",
  readAt: "<value>",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `name`                                                                              | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `employees`                                                                         | *number*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `industry`                                                                          | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `hq`                                                                                | [operations.SizeUnknownPersonHq](../../models/operations/size-unknown-person-hq.md) | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `linkedinUrl`                                                                       | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `website`                                                                           | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `readAt`                                                                            | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |