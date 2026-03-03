# CollectLinkedInPostsResponse

Paginated list of posts from the profile

## Example Usage

```typescript
import { CollectLinkedInPostsResponse } from "bereach/models/operations";

let value: CollectLinkedInPostsResponse = {
  success: false,
  posts: [
    {
      postUrl: "https://slight-mousse.net/",
      text: "<value>",
      date: 13322,
      likesCount: 206224,
      commentsCount: 171386,
      sharesCount: 1950,
      postUrn: "<value>",
      postId: "<id>",
      type: "activity",
    },
  ],
  count: 120519,
  total: 841485,
  start: 865458,
  hasMore: true,
  paginationToken: null,
  previousTotal: null,
  creditsUsed: 653318,
  retryAfter: 694800,
};
```

## Fields

| Field                                                                                                                                                          | Type                                                                                                                                                           | Required                                                                                                                                                       | Description                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                      | *boolean*                                                                                                                                                      | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `posts`                                                                                                                                                        | [operations.CollectLinkedInPostsPost](../../models/operations/collect-linked-in-posts-post.md)[]                                                               | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `count`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `total`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `start`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `hasMore`                                                                                                                                                      | *boolean*                                                                                                                                                      | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `paginationToken`                                                                                                                                              | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `previousTotal`                                                                                                                                                | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | The total from your last call to this endpoint for the same profile (null on first call). Compare with total to detect new posts without client-side tracking. |
| `creditsUsed`                                                                                                                                                  | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                                                           |
| `retryAfter`                                                                                                                                                   | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Seconds to wait before making another call of the same type. 0 means no wait needed.                                                                           |