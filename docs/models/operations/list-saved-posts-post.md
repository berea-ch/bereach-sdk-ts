# ListSavedPostsPost

## Example Usage

```typescript
import { ListSavedPostsPost } from "bereach/models/operations";

let value: ListSavedPostsPost = {
  postUrl: "https://focused-discourse.info",
  postUrn: "<value>",
  postId: "<id>",
  text: "<value>",
  date: 84062,
  likesCount: 487591,
  commentsCount: 937892,
  sharesCount: 215458,
  author: {
    name: "<value>",
    profileUrl: "https://posh-zen.name/",
    publicIdentifier: null,
    profileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `postUrl`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `postUrn`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `postId`                                                                              | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `text`                                                                                | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `date`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `likesCount`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `commentsCount`                                                                       | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `sharesCount`                                                                         | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `author`                                                                              | [operations.ListSavedPostsAuthor](../../models/operations/list-saved-posts-author.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `media`                                                                               | [operations.ListSavedPostsMedia](../../models/operations/list-saved-posts-media.md)   | :heavy_minus_sign:                                                                    | N/A                                                                                   |