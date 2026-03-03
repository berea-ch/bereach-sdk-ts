# SearchLinkedInJobsResponse

List of LinkedIn job listings matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInJobsResponse } from "bereach/models/operations";

let value: SearchLinkedInJobsResponse = {
  success: true,
  category: "jobs",
  items: [
    {
      type: "JOB",
      title: "<value>",
      company: "Davis and Sons",
      companyUrl: "https://secret-veto.info",
      companyLogo: "<value>",
      location: "<value>",
      workplaceType: "<value>",
      postedAt: "<value>",
      jobUrl: "https://pushy-trench.net",
      listingId: "<id>",
    },
  ],
  paging: {
    start: 702907,
    count: 595158,
    total: 190759,
  },
  hasMore: true,
  creditsUsed: 54504,
  retryAfter: 481572,
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `success`                                                                                          | *boolean*                                                                                          | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `category`                                                                                         | [operations.SearchLinkedInJobsCategory](../../models/operations/search-linked-in-jobs-category.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `items`                                                                                            | [operations.SearchLinkedInJobsItem](../../models/operations/search-linked-in-jobs-item.md)[]       | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `paging`                                                                                           | [operations.SearchLinkedInJobsPaging](../../models/operations/search-linked-in-jobs-paging.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `hasMore`                                                                                          | *boolean*                                                                                          | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `creditsUsed`                                                                                      | *number*                                                                                           | :heavy_check_mark:                                                                                 | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).               |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before making another call of the same type. 0 means no wait needed.               |