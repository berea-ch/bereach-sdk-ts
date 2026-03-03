# SearchLinkedInCompaniesResponse

List of LinkedIn companies matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInCompaniesResponse } from "bereach/models/operations";

let value: SearchLinkedInCompaniesResponse = {
  success: false,
  category: "companies",
  items: [],
  paging: {
    start: 902348,
    count: 442491,
    total: 139971,
  },
  hasMore: true,
  creditsUsed: 123084,
  retryAfter: 708841,
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                    | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `category`                                                                                                   | [operations.SearchLinkedInCompaniesCategory](../../models/operations/search-linked-in-companies-category.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `items`                                                                                                      | [operations.SearchLinkedInCompaniesItem](../../models/operations/search-linked-in-companies-item.md)[]       | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `paging`                                                                                                     | [operations.SearchLinkedInCompaniesPaging](../../models/operations/search-linked-in-companies-paging.md)     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `hasMore`                                                                                                    | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `creditsUsed`                                                                                                | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                         |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                         |