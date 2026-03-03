# SearchLinkedInByUrlItemsPost

## Example Usage

```typescript
import { SearchLinkedInByUrlItemsPost } from "bereach/models/operations";

let value: SearchLinkedInByUrlItemsPost = {
  type: "POST",
  postUrl: "https://which-morbidity.com",
  text: "<value>",
  date: 763808,
  likesCount: 115391,
  commentsCount: 352679,
  sharesCount: 764564,
  postUrn: "<value>",
  postId: "<id>",
  author: {
    name: "<value>",
    profileUrl: "https://prestigious-saw.info",
    headline: "<value>",
    profilePicture: "<value>",
    isCompany: true,
  },
  isRepost: true,
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `type`                                                                                                 | [operations.SearchLinkedInByUrlTypePost](../../models/operations/search-linked-in-by-url-type-post.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `postUrl`                                                                                              | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `text`                                                                                                 | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `date`                                                                                                 | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `likesCount`                                                                                           | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `commentsCount`                                                                                        | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `sharesCount`                                                                                          | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `postUrn`                                                                                              | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `postId`                                                                                               | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `author`                                                                                               | [operations.SearchLinkedInByUrlAuthor](../../models/operations/search-linked-in-by-url-author.md)      | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `isRepost`                                                                                             | *boolean*                                                                                              | :heavy_check_mark:                                                                                     | N/A                                                                                                    |