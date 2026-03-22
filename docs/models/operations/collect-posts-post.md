# CollectPostsPost

## Example Usage

```typescript
import { CollectPostsPost } from "bereach/models/operations";

let value: CollectPostsPost = {
  postUrl: "https://fearless-deduction.com",
  text: "<value>",
  date: 510141,
  likesCount: 897757,
  commentsCount: 887746,
  sharesCount: 682971,
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
| `type`                                                                                              | [operations.CollectPostsType](../../models/operations/collect-posts-type.md)                        | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.CollectPostsMedia](../../models/operations/collect-posts-media.md)                      | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |