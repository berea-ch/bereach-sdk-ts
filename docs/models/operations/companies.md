# Companies

## Example Usage

```typescript
import { Companies } from "bereach/models/operations";

let value: Companies = {
  success: true,
  category: "companies",
  items: [],
  paging: {
    start: 347465,
    count: 771442,
    total: 751527,
  },
  hasMore: false,
  creditsUsed: 102383,
  retryAfter: 103254,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | *"companies"*                                                                                                                             | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchSalesNavItemCompany](../../models/operations/search-sales-nav-item-company.md)[]                                        | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchSalesNavPaging2](../../models/operations/search-sales-nav-paging2.md)                                                   | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchSalesNavWarning2](../../models/operations/search-sales-nav-warning2.md)[]                                               | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchSalesNavMeta2](../../models/operations/search-sales-nav-meta2.md)                                                       | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |