# GetCompanyPostsResponse

Company page posts

## Example Usage

```typescript
import { GetCompanyPostsResponse } from "bereach/models/operations";

let value: GetCompanyPostsResponse = {
  success: true,
  posts: [],
  total: 132416,
  creditsUsed: 583148,
  retryAfter: 373913,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `success`                                                                             | *true*                                                                                | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `posts`                                                                               | [operations.GetCompanyPostsPost](../../models/operations/get-company-posts-post.md)[] | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `total`                                                                               | *number*                                                                              | :heavy_check_mark:                                                                    | Total number of posts available.                                                      |
| `creditsUsed`                                                                         | *number*                                                                              | :heavy_check_mark:                                                                    | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).  |
| `retryAfter`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | Seconds to wait before making another call of the same type. 0 means no wait needed.  |