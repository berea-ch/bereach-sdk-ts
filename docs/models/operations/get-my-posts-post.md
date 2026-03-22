# GetMyPostsPost

## Example Usage

```typescript
import { GetMyPostsPost } from "bereach/models/operations";

let value: GetMyPostsPost = {
  postUrl: "https://frequent-hospitalization.net/",
  text: "<value>",
  date: 376647,
  likesCount: 235840,
  commentsCount: 717057,
  sharesCount: 494289,
  postUrn: "<value>",
  postId: "<id>",
  type: "ugcPost",
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `type`                                                                                              | [operations.GetMyPostsType](../../models/operations/get-my-posts-type.md)                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.GetMyPostsMedia](../../models/operations/get-my-posts-media.md)                         | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |