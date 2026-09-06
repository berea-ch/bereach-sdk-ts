# SearchPeopleResponse

List of LinkedIn people matching the search criteria

## Example Usage

```typescript
import { SearchPeopleResponse } from "bereach/models/operations";

let value: SearchPeopleResponse = {
  success: true,
  category: "people",
  items: [],
  paging: {
    start: 729171,
    count: 389121,
    total: 734891,
  },
  hasMore: true,
  creditsUsed: 261104,
  retryAfter: 365627,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | [operations.SearchPeopleCategory](../../models/operations/search-people-category.md)                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchPeopleItem](../../models/operations/search-people-item.md)[]                                                            | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchPeoplePaging](../../models/operations/search-people-paging.md)                                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchPeopleWarning](../../models/operations/search-people-warning.md)[]                                                      | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchPeopleMeta](../../models/operations/search-people-meta.md)                                                              | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |