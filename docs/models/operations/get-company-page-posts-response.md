# GetCompanyPagePostsResponse

Company page posts

## Example Usage

```typescript
import { GetCompanyPagePostsResponse } from "bereach/models/operations";

let value: GetCompanyPagePostsResponse = {
  success: true,
  posts: [
    {
      activityUrn: "<value>",
      postUrl: "https://optimistic-larva.org",
      text: "<value>",
      publishedAt: 3950.94,
      numLikes: 3217.29,
      numComments: 5905.81,
    },
  ],
  total: 215681,
  creditsUsed: 705748,
  retryAfter: 767385,
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `success`                                                                                      | *true*                                                                                         | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `posts`                                                                                        | [operations.GetCompanyPagePostsPost](../../models/operations/get-company-page-posts-post.md)[] | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `total`                                                                                        | *number*                                                                                       | :heavy_check_mark:                                                                             | Total number of posts available.                                                               |
| `creditsUsed`                                                                                  | *number*                                                                                       | :heavy_check_mark:                                                                             | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).           |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before making another call of the same type. 0 means no wait needed.           |