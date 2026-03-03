# GetMyLinkedInPostsResponse

Paginated list of the user's own posts

## Example Usage

```typescript
import { GetMyLinkedInPostsResponse } from "bereach/models/operations";

let value: GetMyLinkedInPostsResponse = {
  success: false,
  posts: [],
  count: 401336,
  total: 836372,
  start: 950669,
  hasMore: false,
  paginationToken: "<value>",
  creditsUsed: 505803,
  retryAfter: 667656,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `success`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `posts`                                                                                       | [operations.GetMyLinkedInPostsPost](../../models/operations/get-my-linked-in-posts-post.md)[] | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `count`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `total`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `start`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `hasMore`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `paginationToken`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `creditsUsed`                                                                                 | *number*                                                                                      | :heavy_check_mark:                                                                            | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).          |
| `retryAfter`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Seconds to wait before making another call of the same type. 0 means no wait needed.          |