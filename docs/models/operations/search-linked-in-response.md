# SearchLinkedInResponse

Search results for the specified category

## Example Usage

```typescript
import { SearchLinkedInResponse } from "bereach/models/operations";

let value: SearchLinkedInResponse = {
  success: true,
  category: "companies",
  items: [],
  paging: {
    start: 436162,
    count: 746156,
    total: 243245,
  },
  hasMore: false,
  creditsUsed: 391662,
  retryAfter: 852821,
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                           | *true*                                                                                                              | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `category`                                                                                                          | [operations.SearchLinkedInCategoryResponseBody](../../models/operations/search-linked-in-category-response-body.md) | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `items`                                                                                                             | *operations.SearchLinkedInItemsUnion*                                                                               | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `paging`                                                                                                            | [operations.SearchLinkedInPaging](../../models/operations/search-linked-in-paging.md)                               | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `hasMore`                                                                                                           | *boolean*                                                                                                           | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `creditsUsed`                                                                                                       | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before making another call of the same type. 0 means no wait needed.                                |