# SearchSalesNavPeopleResponse

Sales Navigator people search results

## Example Usage

```typescript
import { SearchSalesNavPeopleResponse } from "bereach/models/operations";

let value: SearchSalesNavPeopleResponse = {
  success: true,
  category: "people",
  items: [],
  paging: {
    start: 643940,
    count: 778037,
    total: 844626,
  },
  hasMore: true,
  creditsUsed: 281733,
  retryAfter: 278667,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                           | *true*                                                                                                              | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `category`                                                                                                          | [operations.SearchSalesNavPeopleCategoryPeople](../../models/operations/search-sales-nav-people-category-people.md) | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `items`                                                                                                             | [operations.SearchSalesNavPeopleItem](../../models/operations/search-sales-nav-people-item.md)[]                    | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `paging`                                                                                                            | [operations.SearchSalesNavPeoplePaging](../../models/operations/search-sales-nav-people-paging.md)                  | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `hasMore`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `creditsUsed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before making another call of the same type. 0 means no wait needed.                                |