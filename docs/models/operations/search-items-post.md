# SearchItemsPost

## Example Usage

```typescript
import { SearchItemsPost } from "bereach/models/operations";

let value: SearchItemsPost = {
  type: "POST",
  postUrl: "https://suburban-swordfish.org",
  text: "<value>",
  date: 400789,
  likesCount: 73539,
  commentsCount: 846487,
  sharesCount: 956571,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: "https://hollow-unit.biz",
    headline: "<value>",
    profilePicture: "<value>",
    isCompany: true,
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  isRepost: false,
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `type`                                                                                              | [operations.SearchTypePost](../../models/operations/search-type-post.md)                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `author`                                                                                            | [operations.SearchAuthor](../../models/operations/search-author.md)                                 | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `isRepost`                                                                                          | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.SearchMedia](../../models/operations/search-media.md)                                   | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |