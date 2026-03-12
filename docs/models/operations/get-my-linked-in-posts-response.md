# GetMyLinkedInPostsResponse

Paginated list of the user's own posts

## Example Usage

```typescript
import { GetMyLinkedInPostsResponse } from "bereach/models/operations";

let value: GetMyLinkedInPostsResponse = {
  success: true,
  posts: [
    {
      postUrl: "https://important-spear.org/",
      text: "<value>",
      date: 955226,
      likesCount: 177127,
      commentsCount: 505803,
      sharesCount: 667656,
      postUrn: "<value>",
      postId: "<id>",
      type: "ugcPost",
    },
  ],
  count: 32836,
  total: 874592,
  start: 960089,
  hasMore: false,
  paginationToken: null,
  creditsUsed: 498106,
  retryAfter: 364748,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `success`                                                                                     | *true*                                                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `posts`                                                                                       | [operations.GetMyLinkedInPostsPost](../../models/operations/get-my-linked-in-posts-post.md)[] | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `count`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `total`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `start`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `hasMore`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `paginationToken`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `creditsUsed`                                                                                 | *number*                                                                                      | :heavy_check_mark:                                                                            | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).          |
| `retryAfter`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Seconds to wait before making another call of the same type. 0 means no wait needed.          |