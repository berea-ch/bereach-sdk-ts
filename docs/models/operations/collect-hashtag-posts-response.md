# CollectHashtagPostsResponse

Hashtag posts

## Example Usage

```typescript
import { CollectHashtagPostsResponse } from "bereach/models/operations";

let value: CollectHashtagPostsResponse = {
  success: true,
  posts: [],
  total: 374391,
  hasMore: true,
  start: 864672,
  nextStart: 986131,
  creditsUsed: 263221,
  retryAfter: 937145,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `success`                                                                                     | *true*                                                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `posts`                                                                                       | [operations.CollectHashtagPostsPost](../../models/operations/collect-hashtag-posts-post.md)[] | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `total`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `hasMore`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `start`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | Current pagination offset                                                                     |
| `nextStart`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | Offset for next page of results                                                               |
| `creditsUsed`                                                                                 | *number*                                                                                      | :heavy_check_mark:                                                                            | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).          |
| `retryAfter`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Seconds to wait before making another call of the same type. 0 means no wait needed.          |