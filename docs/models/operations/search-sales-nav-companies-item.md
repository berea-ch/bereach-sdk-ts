# SearchSalesNavCompaniesItem

## Example Usage

```typescript
import { SearchSalesNavCompaniesItem } from "bereach/models/operations";

let value: SearchSalesNavCompaniesItem = {
  type: "COMPANY",
  id: "<id>",
  name: "<value>",
  profileUrl: "https://pricey-swanling.biz",
  summary: null,
  industry: "<value>",
  location: "<value>",
  headcount: null,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `type`                                                                                               | [operations.SearchSalesNavCompaniesType](../../models/operations/search-sales-nav-companies-type.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `id`                                                                                                 | *string*                                                                                             | :heavy_check_mark:                                                                                   | Sales Navigator company ID                                                                           |
| `name`                                                                                               | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `profileUrl`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | Sales Navigator company URL                                                                          |
| `summary`                                                                                            | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `industry`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `location`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `headcount`                                                                                          | *string*                                                                                             | :heavy_check_mark:                                                                                   | Employee count or range                                                                              |