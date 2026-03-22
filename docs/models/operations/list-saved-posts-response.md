# ListSavedPostsResponse

Saved posts

## Example Usage

```typescript
import { ListSavedPostsResponse } from "bereach/models/operations";

let value: ListSavedPostsResponse = {
  success: true,
  posts: [
    {
      postUrl: "https://better-department.name/",
      postUrn: "<value>",
      postId: "<id>",
      text: "<value>",
      date: 41956,
      likesCount: 830528,
      commentsCount: 953997,
      sharesCount: 15032,
      author: {
        name: "<value>",
        profileUrl: "https://posh-zen.name/",
        publicIdentifier: null,
        profileUrn: "<value>",
      },
    },
  ],
  total: 21704,
  hasMore: false,
  creditsUsed: 448112,
  retryAfter: 307555,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | [operations.ListSavedPostsPost](../../models/operations/list-saved-posts-post.md)[]  | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |