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

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | [operations.SearchSalesNavPeopleCategoryPeople](../../models/operations/search-sales-nav-people-category-people.md)                       | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchSalesNavPeopleItem](../../models/operations/search-sales-nav-people-item.md)[]                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchSalesNavPeoplePaging](../../models/operations/search-sales-nav-people-paging.md)                                        | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchSalesNavPeopleWarning](../../models/operations/search-sales-nav-people-warning.md)[]                                    | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchSalesNavPeopleMeta](../../models/operations/search-sales-nav-people-meta.md)                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |