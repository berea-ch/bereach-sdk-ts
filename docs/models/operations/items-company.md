# ItemsCompany

## Example Usage

```typescript
import { ItemsCompany } from "bereach/models/operations";

let value: ItemsCompany = {
  type: "COMPANY",
  name: "<value>",
  profileUrl: "https://surprised-sand.name",
  summary: "<value>",
  industry: "<value>",
  location: "<value>",
  followersCount: 309104,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `type`                                                                                                | [operations.SearchByUrlTypeCompany](../../models/operations/search-by-url-type-company.md)            | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `name`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profileUrl`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `summary`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `industry`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `location`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `followersCount`                                                                                      | *number*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `logoUrl`                                                                                             | *string*                                                                                              | :heavy_minus_sign:                                                                                    | Company logo URL when LinkedIn surfaces it on the result entity. Display this in the company card.    |
| `lane`                                                                                                | [operations.SearchByUrlLane2](../../models/operations/search-by-url-lane2.md)                         | :heavy_minus_sign:                                                                                    | Present when this row came from the public lane covering for the connected account. Public data only. |