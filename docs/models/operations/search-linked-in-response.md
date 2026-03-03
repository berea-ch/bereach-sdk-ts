# SearchLinkedInResponse

Search results for the specified category

## Example Usage

```typescript
import { SearchLinkedInResponse } from "bereach/models/operations";

let value: SearchLinkedInResponse = {
  success: false,
  category: "companies",
  items: [],
  paging: {
    start: 746156,
    count: 243245,
    total: 826762,
  },
  hasMore: true,
  creditsUsed: 852821,
  retryAfter: 28235,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `category`                                                                                                          | [operations.SearchLinkedInCategoryResponseBody](../../models/operations/search-linked-in-category-response-body.md) | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `items`                                                                                                             | *operations.SearchLinkedInItemsUnion*                                                                               | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `paging`                                                                                                            | [operations.SearchLinkedInPaging](../../models/operations/search-linked-in-paging.md)                               | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `hasMore`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `creditsUsed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before making another call of the same type. 0 means no wait needed.                                |