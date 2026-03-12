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
      id: "<id>",
      name: "<value>",
      profileUrl: "https://nocturnal-netsuke.biz/",
      summary: "<value>",
      industry: "<value>",
      location: "<value>",
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

| Field                                                                                                                           | Type                                                                                                                            | Required                                                                                                                        | Description                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                       | *true*                                                                                                                          | :heavy_check_mark:                                                                                                              | N/A                                                                                                                             |
| `category`                                                                                                                      | [operations.SearchSalesNavCompaniesCategoryCompanies](../../models/operations/search-sales-nav-companies-category-companies.md) | :heavy_check_mark:                                                                                                              | N/A                                                                                                                             |
| `items`                                                                                                                         | [operations.SearchSalesNavCompaniesItem](../../models/operations/search-sales-nav-companies-item.md)[]                          | :heavy_check_mark:                                                                                                              | N/A                                                                                                                             |
| `paging`                                                                                                                        | [operations.SearchSalesNavCompaniesPaging](../../models/operations/search-sales-nav-companies-paging.md)                        | :heavy_check_mark:                                                                                                              | N/A                                                                                                                             |
| `hasMore`                                                                                                                       | *boolean*                                                                                                                       | :heavy_check_mark:                                                                                                              | N/A                                                                                                                             |
| `creditsUsed`                                                                                                                   | *number*                                                                                                                        | :heavy_check_mark:                                                                                                              | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                            |
| `retryAfter`                                                                                                                    | *number*                                                                                                                        | :heavy_check_mark:                                                                                                              | Seconds to wait before making another call of the same type. 0 means no wait needed.                                            |