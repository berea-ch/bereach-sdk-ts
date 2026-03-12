# SearchSalesNavItemCompany

## Example Usage

```typescript
import { SearchSalesNavItemCompany } from "bereach/models/operations";

let value: SearchSalesNavItemCompany = {
  type: "COMPANY",
  id: "<id>",
  name: "<value>",
  profileUrl: "https://wilted-cheetah.name/",
  summary: "<value>",
  industry: "<value>",
  location: "<value>",
  headcount: null,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `type`                                                                                           | [operations.SearchSalesNavTypeCompany](../../models/operations/search-sales-nav-type-company.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `id`                                                                                             | *string*                                                                                         | :heavy_check_mark:                                                                               | Sales Navigator company ID                                                                       |
| `name`                                                                                           | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `profileUrl`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | Sales Navigator company URL                                                                      |
| `summary`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `industry`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `location`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `headcount`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | Employee count or range                                                                          |