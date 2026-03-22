# SearchPostsItem

## Example Usage

```typescript
import { SearchPostsItem } from "bereach/models/operations";

let value: SearchPostsItem = {
  type: "POST",
  postUrl: "https://royal-peony.info/",
  text: "<value>",
  date: 759390,
  likesCount: 578550,
  commentsCount: 599433,
  sharesCount: 339851,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: "https://colossal-filter.name/",
    headline: "<value>",
    profilePicture: "<value>",
    isCompany: false,
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  isRepost: false,
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `type`                                                                                              | [operations.SearchPostsType](../../models/operations/search-posts-type.md)                          | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrl`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `date`                                                                                              | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `likesCount`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `commentsCount`                                                                                     | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `sharesCount`                                                                                       | *number*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postUrn`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `postId`                                                                                            | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `author`                                                                                            | [operations.SearchPostsAuthor](../../models/operations/search-posts-author.md)                      | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `isRepost`                                                                                          | *boolean*                                                                                           | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.SearchPostsMedia](../../models/operations/search-posts-media.md)                        | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |