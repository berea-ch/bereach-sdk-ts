# SearchCompaniesResponse

List of LinkedIn companies matching the search criteria

## Example Usage

```typescript
import { SearchCompaniesResponse } from "bereach/models/operations";

let value: SearchCompaniesResponse = {
  success: true,
  category: "companies",
  items: [],
  paging: {
    start: 931965,
    count: 28391,
    total: 271441,
  },
  hasMore: false,
  creditsUsed: 746537,
  retryAfter: 296169,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `success`                                                                                  | *true*                                                                                     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `category`                                                                                 | [operations.SearchCompaniesCategory](../../models/operations/search-companies-category.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `items`                                                                                    | [operations.SearchCompaniesItem](../../models/operations/search-companies-item.md)[]       | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `paging`                                                                                   | [operations.SearchCompaniesPaging](../../models/operations/search-companies-paging.md)     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `hasMore`                                                                                  | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `creditsUsed`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).       |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before making another call of the same type. 0 means no wait needed.       |