# PublicFindJobsRequest

## Example Usage

```typescript
import { PublicFindJobsRequest } from "bereach/models/operations";

let value: PublicFindJobsRequest = {
  filters: {},
};
```

## Fields

| Field                                                                                                                                                     | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `filters`                                                                                                                                                 | [operations.PublicFindJobsFilters](../../models/operations/public-find-jobs-filters.md)                                                                   | :heavy_check_mark:                                                                                                                                        | Search facets. Provide at least one of title, company, location, industry, or keywords.                                                                   |
| `limit`                                                                                                                                                   | *number*                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                        | Target number of job postings.                                                                                                                            |
| `more`                                                                                                                                                    | *boolean*                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                        | Continue past what an earlier call on this same ask already returned, instead of returning it again. What counts as already returned is kept server side. |