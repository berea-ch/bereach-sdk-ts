# CompanyPagePostsPost

## Example Usage

```typescript
import { CompanyPagePostsPost } from "bereach/models/operations";

let value: CompanyPagePostsPost = {
  activityUrn: "<value>",
  postUrl: "https://quarrelsome-pigpen.name",
  text: "<value>",
  publishedAt: 7245.3,
  numLikes: 2251.52,
  numComments: 3158.6,
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