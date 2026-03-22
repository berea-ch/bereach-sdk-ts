# GetCompanyPostsPost

## Example Usage

```typescript
import { GetCompanyPostsPost } from "bereach/models/operations";

let value: GetCompanyPostsPost = {
  activityUrn: "<value>",
  postUrl: "https://simple-intellect.name/",
  text: "<value>",
  publishedAt: 3349.18,
  numLikes: 2403.81,
  numComments: 9945.65,
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