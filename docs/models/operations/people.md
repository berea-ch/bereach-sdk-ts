# People

## Example Usage

```typescript
import { People } from "bereach/models/operations";

let value: People = {
  success: true,
  category: "people",
  items: [],
  paging: {
    start: 950851,
    count: 201379,
    total: 28084,
  },
  hasMore: true,
  creditsUsed: 523865,
  retryAfter: 697277,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | *"people"*                                                                                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchSalesNavItemPeople](../../models/operations/search-sales-nav-item-people.md)[]                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchSalesNavPaging1](../../models/operations/search-sales-nav-paging1.md)                                                   | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchSalesNavWarning1](../../models/operations/search-sales-nav-warning1.md)[]                                               | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchSalesNavMeta1](../../models/operations/search-sales-nav-meta1.md)                                                       | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |