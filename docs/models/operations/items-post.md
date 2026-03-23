# ItemsPost

## Example Usage

```typescript
import { ItemsPost } from "bereach/models/operations";

let value: ItemsPost = {
  type: "POST",
  postUrl: "https://elegant-pear.name/",
  text: "<value>",
  date: 76696,
  likesCount: 39647,
  commentsCount: 495127,
  sharesCount: 992575,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: "https://low-cap.org/",
    headline: null,
    profilePicture: "<value>",
    isCompany: true,
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  isRepost: true,
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `type`                                                                                              | [operations.ItemsTypePost](../../models/operations/items-type-post.md)                              | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `author`                                                                                            | [operations.ItemsAuthor](../../models/operations/items-author.md)                                   | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `isRepost`                                                                                          | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.ItemsMedia](../../models/operations/items-media.md)                                     | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |