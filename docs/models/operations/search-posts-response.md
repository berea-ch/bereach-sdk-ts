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
      likesCount: 331248,
      commentsCount: 626729,
      sharesCount: 277560,
      postUrn: "<value>",
      postId: "<id>",
      type: "POST",
      author: {
        name: "<value>",
        profileUrl: "https://colossal-filter.name/",
        headline: "<value>",
        profilePicture: "<value>",
        isCompany: false,
        publicIdentifier: "<value>",
        profileUrn: "<value>",
      },
      isRepost: true,
    },
  ],
  paging: {
    start: 56909,
    count: 253278,
    total: 384396,
  },
  hasMore: false,
  creditsUsed: 457806,
  retryAfter: 822102,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `category`                                                                                                                                | [operations.SearchPostsCategory](../../models/operations/search-posts-category.md)                                                        | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchPostsItem](../../models/operations/search-posts-item.md)[]                                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchPostsPaging](../../models/operations/search-posts-paging.md)                                                            | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchPostsWarning](../../models/operations/search-posts-warning.md)[]                                                        | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchPostsMeta](../../models/operations/search-posts-meta.md)                                                                | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |