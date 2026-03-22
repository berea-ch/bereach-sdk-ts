# CollectHashtagPostsPost

## Example Usage

```typescript
import { CollectHashtagPostsPost } from "bereach/models/operations";

let value: CollectHashtagPostsPost = {
  postUrl: "https://grouchy-sonnet.info",
  postUrn: "<value>",
  text: "<value>",
  date: 742633,
  likesCount: 2848,
  commentsCount: 226094,
  sharesCount: 783310,
  author: {
    name: "<value>",
    profileUrl: "https://regular-verve.biz/",
    publicIdentifier: null,
    profileUrn: null,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `postUrn`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `text`                                                                                          | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `date`                                                                                          | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `likesCount`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `commentsCount`                                                                                 | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `sharesCount`                                                                                   | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `author`                                                                                        | [operations.CollectHashtagPostsAuthor](../../models/operations/collect-hashtag-posts-author.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `media`                                                                                         | [operations.CollectHashtagPostsMedia](../../models/operations/collect-hashtag-posts-media.md)   | :heavy_minus_sign:                                                                              | N/A                                                                                             |