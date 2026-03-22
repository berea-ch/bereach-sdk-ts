# SearchResponse

Search results for the specified category

## Example Usage

```typescript
import { SearchResponse } from "bereach/models/operations";

let value: SearchResponse = {
  success: true,
  category: "people",
  items: [],
  paging: {
    start: 871542,
    count: 595646,
    total: 468591,
  },
  hasMore: false,
  creditsUsed: 318424,
  retryAfter: 577773,
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `success`                                                                                         | *true*                                                                                            | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `category`                                                                                        | [operations.SearchCategoryResponseBody](../../models/operations/search-category-response-body.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `items`                                                                                           | *operations.SearchItemsUnion*                                                                     | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `paging`                                                                                          | [operations.SearchPaging](../../models/operations/search-paging.md)                               | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `hasMore`                                                                                         | *boolean*                                                                                         | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `creditsUsed`                                                                                     | *number*                                                                                          | :heavy_check_mark:                                                                                | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).              |
| `retryAfter`                                                                                      | *number*                                                                                          | :heavy_check_mark:                                                                                | Seconds to wait before making another call of the same type. 0 means no wait needed.              |