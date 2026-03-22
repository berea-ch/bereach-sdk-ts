# SearchJobsResponse

List of LinkedIn job listings matching the search criteria

## Example Usage

```typescript
import { SearchJobsResponse } from "bereach/models/operations";

let value: SearchJobsResponse = {
  success: true,
  category: "jobs",
  items: [],
  paging: {
    start: 968233,
    count: 443508,
    total: 906771,
  },
  hasMore: false,
  creditsUsed: 595366,
  retryAfter: 173084,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `category`                                                                           | [operations.SearchJobsCategory](../../models/operations/search-jobs-category.md)     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `items`                                                                              | [operations.SearchJobsItem](../../models/operations/search-jobs-item.md)[]           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `paging`                                                                             | [operations.SearchJobsPaging](../../models/operations/search-jobs-paging.md)         | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |