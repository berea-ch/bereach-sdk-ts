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

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `savedSearches`                                                                                                                           | [operations.SavedSearch](../../models/operations/saved-search.md)[]                                                                       | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ListSalesNavSavedSearchesMeta](../../models/operations/list-sales-nav-saved-searches-meta.md)                                 | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |