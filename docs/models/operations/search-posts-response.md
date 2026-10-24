# SearchPostsResponse

List of LinkedIn posts matching the search criteria

## Example Usage

```typescript
import { SearchPostsResponse } from "bereach/models/operations";

let value: SearchPostsResponse = {
  success: true,
  category: "posts",
  items: [
    {
      postUrl: "https://upset-cook.com",
      text: "<value>",
      date: 630882,
      likesCount: 626729,
      commentsCount: 482176,
      sharesCount: null,
      postUrn: "<value>",
      postId: "<id>",
      type: "POST",
      author: {
        name: "<value>",
        profileUrl: "https://miserly-cafe.net/",
        headline: "<value>",
        profilePicture: "<value>",
        isCompany: true,
        publicIdentifier: "<value>",
        profileUrn: "<value>",
      },
      isRepost: true,
    },
  ],
  paging: {
    start: 384396,
    count: 821756,
    total: 457806,
  },
  hasMore: false,
  creditsUsed: 201860,
  retryAfter: 498291,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `category`                                                                                                                        | [operations.SearchPostsCategory](../../models/operations/search-posts-category.md)                                                | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `items`                                                                                                                           | [operations.SearchPostsItem](../../models/operations/search-posts-item.md)[]                                                      | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `paging`                                                                                                                          | [operations.SearchPostsPaging](../../models/operations/search-posts-paging.md)                                                    | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `hasMore`                                                                                                                         | *boolean*                                                                                                                         | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `warnings`                                                                                                                        | [operations.SearchPostsWarning](../../models/operations/search-posts-warning.md)[]                                                | :heavy_minus_sign:                                                                                                                | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                             |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |