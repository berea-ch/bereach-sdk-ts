# SearchLinkedInPostsResponse

List of LinkedIn posts matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInPostsResponse } from "bereach/models/operations";

let value: SearchLinkedInPostsResponse = {
  success: true,
  category: "posts",
  items: [],
  paging: {
    start: 738455,
    count: 537600,
    total: 501889,
  },
  hasMore: false,
  creditsUsed: 514601,
  retryAfter: 682361,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `success`                                                                                            | *true*                                                                                               | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `category`                                                                                           | [operations.SearchLinkedInPostsCategory](../../models/operations/search-linked-in-posts-category.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `items`                                                                                              | [operations.SearchLinkedInPostsItem](../../models/operations/search-linked-in-posts-item.md)[]       | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `paging`                                                                                             | [operations.SearchLinkedInPostsPaging](../../models/operations/search-linked-in-posts-paging.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `hasMore`                                                                                            | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `creditsUsed`                                                                                        | *number*                                                                                             | :heavy_check_mark:                                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                 |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed.                 |