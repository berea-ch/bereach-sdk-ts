# SearchLinkedInPeopleResponse

List of LinkedIn people matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInPeopleResponse } from "bereach/models/operations";

let value: SearchLinkedInPeopleResponse = {
  success: true,
  category: "people",
  items: [
    {
      type: "PEOPLE",
      name: "<value>",
      profileUrl: "https://puzzled-someplace.biz/",
      headline: "<value>",
      location: "<value>",
      profilePicture: "<value>",
      networkDistance: "DISTANCE_2",
      currentPositions: [
        {
          company: "Ernser, Gibson and Larson",
          role: "<value>",
        },
      ],
    },
  ],
  paging: {
    start: 4718,
    count: 336888,
    total: 306421,
  },
  hasMore: false,
  creditsUsed: 561882,
  retryAfter: 629348,
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `success`                                                                                              | *true*                                                                                                 | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `category`                                                                                             | [operations.SearchLinkedInPeopleCategory](../../models/operations/search-linked-in-people-category.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `items`                                                                                                | [operations.SearchLinkedInPeopleItem](../../models/operations/search-linked-in-people-item.md)[]       | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `paging`                                                                                               | [operations.SearchLinkedInPeoplePaging](../../models/operations/search-linked-in-people-paging.md)     | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `hasMore`                                                                                              | *boolean*                                                                                              | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `creditsUsed`                                                                                          | *number*                                                                                               | :heavy_check_mark:                                                                                     | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                   |
| `retryAfter`                                                                                           | *number*                                                                                               | :heavy_check_mark:                                                                                     | Seconds to wait before making another call of the same type. 0 means no wait needed.                   |