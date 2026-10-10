# SearchCompaniesItem

## Example Usage

```typescript
import { SearchCompaniesItem } from "bereach/models/operations";

let value: SearchCompaniesItem = {
  type: "COMPANY",
  name: "<value>",
  profileUrl: "https://austere-challenge.info",
  summary: "<value>",
  industry: "<value>",
  location: "<value>",
  followersCount: 770990,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `type`                                                                                                | [operations.SearchCompaniesType](../../models/operations/search-companies-type.md)                    | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `name`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profileUrl`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `summary`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `industry`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `location`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `followersCount`                                                                                      | *number*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `logoUrl`                                                                                             | *string*                                                                                              | :heavy_minus_sign:                                                                                    | Company logo URL when LinkedIn surfaces it on the result entity. Display this in the company card.    |
| `lane`                                                                                                | [operations.SearchCompaniesLane](../../models/operations/search-companies-lane.md)                    | :heavy_minus_sign:                                                                                    | Present when this row came from the public lane covering for the connected account. Public data only. |