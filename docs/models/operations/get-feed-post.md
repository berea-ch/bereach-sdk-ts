# GetFeedPost

## Example Usage

```typescript
import { GetFeedPost } from "bereach/models/operations";

let value: GetFeedPost = {
  postUrl: "https://ambitious-lifestyle.biz/",
  text: "<value>",
  date: 364030,
  likesCount: 826267,
  commentsCount: 107988,
  sharesCount: 375589,
  postUrn: "<value>",
  postId: "<id>",
  type: "activity",
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
| `type`                                                                                              | [operations.GetFeedType](../../models/operations/get-feed-type.md)                                  | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `media`                                                                                             | [operations.GetFeedMedia](../../models/operations/get-feed-media.md)                                | :heavy_minus_sign:                                                                                  | Media attached to the post (image, video, document, or article). Absent when the post is text-only. |