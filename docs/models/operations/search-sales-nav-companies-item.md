# SearchSalesNavCompaniesItem

## Example Usage

```typescript
import { SearchSalesNavCompaniesItem } from "bereach/models/operations";

let value: SearchSalesNavCompaniesItem = {
  type: "COMPANY",
  name: "<value>",
  profileUrl: "https://pricey-swanling.biz",
  summary: null,
  industry: "<value>",
  location: "<value>",
  id: "<id>",
  headcount: null,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `type`                                                                                                | [operations.SearchSalesNavCompaniesType](../../models/operations/search-sales-nav-companies-type.md)  | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `name`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profileUrl`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `summary`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `industry`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `location`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `logoUrl`                                                                                             | *string*                                                                                              | :heavy_minus_sign:                                                                                    | Company logo URL when LinkedIn surfaces it on the result entity. Display this in the company card.    |
| `lane`                                                                                                | [operations.SearchSalesNavCompaniesLane](../../models/operations/search-sales-nav-companies-lane.md)  | :heavy_minus_sign:                                                                                    | Present when this row came from the public lane covering for the connected account. Public data only. |
| `id`                                                                                                  | *string*                                                                                              | :heavy_check_mark:                                                                                    | Sales Navigator company ID                                                                            |
| `headcount`                                                                                           | *string*                                                                                              | :heavy_check_mark:                                                                                    | Employee count or range                                                                               |