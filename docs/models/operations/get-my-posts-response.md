# GetMyPostsResponse

Paginated list of the user's own posts

## Example Usage

```typescript
import { GetMyPostsResponse } from "bereach/models/operations";

let value: GetMyPostsResponse = {
  success: true,
  posts: [
    {
      postUrl: "https://superior-space.name",
      text: "<value>",
      date: 903307,
      likesCount: 363747,
      commentsCount: 80601,
      sharesCount: 129652,
      postUrn: "<value>",
      postId: "<id>",
      type: "activity",
    },
  ],
  count: 432143,
  total: 78283,
  start: 973857,
  hasMore: true,
  paginationToken: "<value>",
  creditsUsed: 811523,
  retryAfter: 353791,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | [operations.GetMyPostsPost](../../models/operations/get-my-posts-post.md)[]          | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `count`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `start`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `paginationToken`                                                                    | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |