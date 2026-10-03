# CompanyPagePostsResponse

Company page posts

## Example Usage

```typescript
import { CompanyPagePostsResponse } from "bereach/models/operations";

let value: CompanyPagePostsResponse = {
  success: true,
  posts: [
    {
      activityUrn: "<value>",
      postUrl: "https://indolent-sticker.com",
      text: "<value>",
      publishedAt: 6443.6,
      numLikes: 9861.64,
      numComments: 3096.93,
    },
  ],
  total: 59209,
  creditsUsed: 536369,
  retryAfter: 750157,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `posts`                                                                                                                                   | [operations.CompanyPagePostsPost](../../models/operations/company-page-posts-post.md)[]                                                   | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total number of posts available.                                                                                                          |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CompanyPagePostsMeta](../../models/operations/company-page-posts-meta.md)                                                     | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |