# SearchSalesNavCompaniesResponse

Sales Navigator company search results

## Example Usage

```typescript
import { SearchSalesNavCompaniesResponse } from "bereach/models/operations";

let value: SearchSalesNavCompaniesResponse = {
  success: true,
  category: "companies",
  items: [
    {
      type: "COMPANY",
      name: "<value>",
      profileUrl: "https://nocturnal-netsuke.biz/",
      summary: "<value>",
      industry: "<value>",
      location: "<value>",
      id: "<id>",
      headcount: "<value>",
    },
  ],
  paging: {
    start: 763373,
    count: 784738,
    total: 201004,
  },
  hasMore: false,
  creditsUsed: 490771,
  retryAfter: 530123,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | [operations.SearchSalesNavCompaniesCategoryCompanies](../../models/operations/search-sales-nav-companies-category-companies.md)           | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchSalesNavCompaniesItem](../../models/operations/search-sales-nav-companies-item.md)[]                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchSalesNavCompaniesPaging](../../models/operations/search-sales-nav-companies-paging.md)                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchSalesNavCompaniesWarning](../../models/operations/search-sales-nav-companies-warning.md)[]                              | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchSalesNavCompaniesMeta](../../models/operations/search-sales-nav-companies-meta.md)                                      | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |