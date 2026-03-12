# SearchLinkedInCompaniesResponse

List of LinkedIn companies matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInCompaniesResponse } from "bereach/models/operations";

let value: SearchLinkedInCompaniesResponse = {
  success: true,
  category: "companies",
  items: [
    {
      type: "COMPANY",
      name: "<value>",
      profileUrl: null,
      summary: "<value>",
      industry: "<value>",
      location: "<value>",
      followersCount: null,
    },
  ],
  paging: {
    start: 123084,
    count: 708841,
    total: 233268,
  },
  hasMore: true,
  creditsUsed: 133989,
  retryAfter: 39570,
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                    | *true*                                                                                                       | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `category`                                                                                                   | [operations.SearchLinkedInCompaniesCategory](../../models/operations/search-linked-in-companies-category.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `items`                                                                                                      | [operations.SearchLinkedInCompaniesItem](../../models/operations/search-linked-in-companies-item.md)[]       | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `paging`                                                                                                     | [operations.SearchLinkedInCompaniesPaging](../../models/operations/search-linked-in-companies-paging.md)     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `hasMore`                                                                                                    | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `creditsUsed`                                                                                                | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                         |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before making another call of the same type. 0 means no wait needed.                         |