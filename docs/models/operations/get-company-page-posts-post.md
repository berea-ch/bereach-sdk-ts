# GetCompanyPagePostsPost

## Example Usage

```typescript
import { GetCompanyPagePostsPost } from "bereach/models/operations";

let value: GetCompanyPagePostsPost = {
  activityUrn: "<value>",
  postUrl: "https://fake-heroine.org",
  text: null,
  publishedAt: 4407.81,
  numLikes: 9106.18,
  numComments: null,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `activityUrn`                                         | *string*                                              | :heavy_check_mark:                                    | LinkedIn activity URN for this post.                  |
| `postUrl`                                             | *string*                                              | :heavy_check_mark:                                    | Direct URL to the post on LinkedIn.                   |
| `text`                                                | *string*                                              | :heavy_check_mark:                                    | Post text content (null if media-only).               |
| `publishedAt`                                         | *number*                                              | :heavy_check_mark:                                    | Unix timestamp in milliseconds (null if unavailable). |
| `numLikes`                                            | *number*                                              | :heavy_check_mark:                                    | Number of likes/reactions.                            |
| `numComments`                                         | *number*                                              | :heavy_check_mark:                                    | Number of comments.                                   |