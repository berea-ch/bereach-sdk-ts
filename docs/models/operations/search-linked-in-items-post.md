# SearchLinkedInItemsPost

## Example Usage

```typescript
import { SearchLinkedInItemsPost } from "bereach/models/operations";

let value: SearchLinkedInItemsPost = {
  type: "POST",
  postUrl: "https://querulous-finger.net/",
  text: "<value>",
  date: 373204,
  likesCount: 464026,
  commentsCount: 14557,
  sharesCount: 869476,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: null,
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
| `type`                                                                                              | [operations.SearchLinkedInTypePost](../../models/operations/search-linked-in-type-post.md)          | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `author`                                                                                            | [operations.SearchLinkedInAuthor](../../models/operations/search-linked-in-author.md)               | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `isRepost`                                                                                          | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.SearchLinkedInMedia](../../models/operations/search-linked-in-media.md)                 | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |