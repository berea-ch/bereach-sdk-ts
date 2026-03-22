# SearchByUrlItemsPost

## Example Usage

```typescript
import { SearchByUrlItemsPost } from "bereach/models/operations";

let value: SearchByUrlItemsPost = {
  type: "POST",
  postUrl: "https://rough-decision.biz/",
  text: "<value>",
  date: 654138,
  likesCount: 807155,
  commentsCount: 422717,
  sharesCount: 612299,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: "https://wide-eyed-violin.com",
    headline: "<value>",
    profilePicture: "<value>",
    isCompany: false,
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  isRepost: true,
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `type`                                                                                              | [operations.SearchByUrlTypePost](../../models/operations/search-by-url-type-post.md)                | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `author`                                                                                            | [operations.SearchByUrlAuthor](../../models/operations/search-by-url-author.md)                     | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `isRepost`                                                                                          | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.SearchByUrlMedia](../../models/operations/search-by-url-media.md)                       | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |