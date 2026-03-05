# SearchLinkedInByUrlResponse

Search results parsed from the LinkedIn URL

## Example Usage

```typescript
import { SearchLinkedInByUrlResponse } from "bereach/models/operations";

let value: SearchLinkedInByUrlResponse = {
  success: true,
  category: "jobs",
  items: [
    {
      type: "COMPANY",
      name: "<value>",
      profileUrl: "https://tiny-bathrobe.biz",
      summary: "<value>",
      industry: "<value>",
      location: null,
      followersCount: 993595,
    },
  ],
  paging: {
    start: 913942,
    count: 318758,
    total: 847473,
  },
  hasMore: false,
  creditsUsed: 332652,
  retryAfter: 299060,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `success`                                                                                             | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `category`                                                                                            | [operations.SearchLinkedInByUrlCategory](../../models/operations/search-linked-in-by-url-category.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `items`                                                                                               | *operations.SearchLinkedInByUrlItemsUnion*                                                            | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `paging`                                                                                              | [operations.SearchLinkedInByUrlPaging](../../models/operations/search-linked-in-by-url-paging.md)     | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `hasMore`                                                                                             | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `creditsUsed`                                                                                         | *number*                                                                                              | :heavy_check_mark:                                                                                    | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                  |
| `retryAfter`                                                                                          | *number*                                                                                              | :heavy_check_mark:                                                                                    | Seconds to wait before making another call of the same type. 0 means no wait needed.                  |