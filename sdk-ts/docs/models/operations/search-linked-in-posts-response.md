# SearchLinkedInPostsResponse

List of LinkedIn posts matching the search criteria

## Example Usage

```typescript
import { SearchLinkedInPostsResponse } from "bereach/models/operations";

let value: SearchLinkedInPostsResponse = {
  success: true,
  category: "posts",
  items: [
    {
      type: "POST",
      postUrl: "https://mature-making.name",
      text: "<value>",
      date: 682361,
      likesCount: 39530,
      commentsCount: 407238,
      sharesCount: 376548,
      postUrn: "<value>",
      postId: "<id>",
      author: {
        name: "<value>",
        profileUrl: "https://svelte-sport.name/",
        headline: "<value>",
        profilePicture: "<value>",
        isCompany: true,
      },
      isRepost: true,
    },
  ],
  paging: {
    start: 11792,
    count: 452366,
    total: 225663,
  },
  hasMore: true,
  creditsUsed: 477463,
  retryAfter: 509810,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `success`                                                                                            | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `category`                                                                                           | [operations.SearchLinkedInPostsCategory](../../models/operations/search-linked-in-posts-category.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `items`                                                                                              | [operations.SearchLinkedInPostsItem](../../models/operations/search-linked-in-posts-item.md)[]       | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `paging`                                                                                             | [operations.SearchLinkedInPostsPaging](../../models/operations/search-linked-in-posts-paging.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `hasMore`                                                                                            | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `creditsUsed`                                                                                        | *number*                                                                                             | :heavy_check_mark:                                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                 |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed.                 |