# SearchLinkedInByUrlResponse

Search results parsed from the LinkedIn URL

## Example Usage

```typescript
import { SearchLinkedInByUrlResponse } from "bereach/models/operations";

let value: SearchLinkedInByUrlResponse = {
  success: true,
  category: "people",
  items: [
    {
      type: "JOB",
      title: "<value>",
      company: "Ondricka and Sons",
      companyUrl: null,
      companyLogo: "<value>",
      location: "<value>",
      workplaceType: "<value>",
      postedAt: null,
      jobUrl: "https://yellowish-tinderbox.biz",
      listingId: "<id>",
    },
  ],
  paging: {
    start: 847473,
    count: 874101,
    total: 332652,
  },
  hasMore: true,
  creditsUsed: 539086,
  retryAfter: 127049,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `success`                                                                                             | *true*                                                                                                | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `category`                                                                                            | [operations.SearchLinkedInByUrlCategory](../../models/operations/search-linked-in-by-url-category.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `items`                                                                                               | *operations.SearchLinkedInByUrlItemsUnion*                                                            | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `paging`                                                                                              | [operations.SearchLinkedInByUrlPaging](../../models/operations/search-linked-in-by-url-paging.md)     | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `hasMore`                                                                                             | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `creditsUsed`                                                                                         | *number*                                                                                              | :heavy_check_mark:                                                                                    | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                  |
| `retryAfter`                                                                                          | *number*                                                                                              | :heavy_check_mark:                                                                                    | Seconds to wait before making another call of the same type. 0 means no wait needed.                  |