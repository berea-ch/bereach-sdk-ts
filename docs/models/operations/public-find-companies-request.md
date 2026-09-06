# PublicFindCompaniesRequest

## Example Usage

```typescript
import { PublicFindCompaniesRequest } from "bereach/models/operations";

let value: PublicFindCompaniesRequest = {
  filters: {},
};
```

## Fields

| Field                                                                                                                                       | Type                                                                                                                                        | Required                                                                                                                                    | Description                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `filters`                                                                                                                                   | [operations.PublicFindCompaniesFilters](../../models/operations/public-find-companies-filters.md)                                           | :heavy_check_mark:                                                                                                                          | Search facets. Provide at least one company-level facet: company, industry, location, or keywords. A role or title cannot select companies. |
| `limit`                                                                                                                                     | *number*                                                                                                                                    | :heavy_minus_sign:                                                                                                                          | Target number of companies.                                                                                                                 |
| `more`                                                                                                                                      | *boolean*                                                                                                                                   | :heavy_minus_sign:                                                                                                                          | Continue an earlier call on this same ask instead of returning the same companies.                                                          |