# SearchByUrlResponse

Search results parsed from the LinkedIn URL

## Example Usage

```typescript
import { SearchByUrlResponse } from "bereach/models/operations";

let value: SearchByUrlResponse = {
  success: true,
  category: "posts",
  items: [],
  paging: {
    start: 489545,
    count: 70087,
    total: 782351,
  },
  hasMore: false,
  creditsUsed: 380821,
  retryAfter: 562660,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `category`                                                                           | [operations.SearchByUrlCategory](../../models/operations/search-by-url-category.md)  | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `items`                                                                              | *operations.SearchByUrlItemsUnion*                                                   | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `paging`                                                                             | [operations.SearchByUrlPaging](../../models/operations/search-by-url-paging.md)      | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |