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

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `category`                                                                           | [operations.SearchPeopleCategory](../../models/operations/search-people-category.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `items`                                                                              | [operations.SearchPeopleItem](../../models/operations/search-people-item.md)[]       | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `paging`                                                                             | [operations.SearchPeoplePaging](../../models/operations/search-people-paging.md)     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |