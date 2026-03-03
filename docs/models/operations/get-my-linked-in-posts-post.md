# GetMyLinkedInPostsPost

## Example Usage

```typescript
import { GetMyLinkedInPostsPost } from "bereach/models/operations";

let value: GetMyLinkedInPostsPost = {
  postUrl: "https://silky-depot.org",
  text: "<value>",
  date: 593254,
  likesCount: 609580,
  commentsCount: 665145,
  sharesCount: 323179,
  postUrn: "<value>",
  postId: "<id>",
  type: "ugcPost",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                   | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `text`                                                                                      | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `date`                                                                                      | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `likesCount`                                                                                | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `commentsCount`                                                                             | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `sharesCount`                                                                               | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `postUrn`                                                                                   | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `postId`                                                                                    | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `type`                                                                                      | [operations.GetMyLinkedInPostsType](../../models/operations/get-my-linked-in-posts-type.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |