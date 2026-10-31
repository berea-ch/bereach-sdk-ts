# ListSalesNavSavedSearchesResponse

User's saved searches.

## Example Usage

```typescript
import { ListSalesNavSavedSearchesResponse } from "bereach/models/operations";

let value: ListSalesNavSavedSearchesResponse = {
  success: true,
  savedSearches: [
    {
      id: "<id>",
      name: "<value>",
      category: "people",
      savedSearchUrl: "https://buzzing-makeover.com",
      newResultsCount: 104627,
      lastUsedAt: "<value>",
    },
  ],
  count: 708688,
  creditsUsed: 10251,
  retryAfter: 724318,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `savedSearches`                                                                                                                   | [operations.SavedSearch](../../models/operations/saved-search.md)[]                                                               | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `count`                                                                                                                           | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |