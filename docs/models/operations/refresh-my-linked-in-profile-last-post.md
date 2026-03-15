# RefreshMyLinkedInProfileLastPost

## Example Usage

```typescript
import { RefreshMyLinkedInProfileLastPost } from "bereach/models/operations";

let value: RefreshMyLinkedInProfileLastPost = {
  postUrl: "https://velvety-populist.org",
  text: "<value>",
  date: 806217,
  likesCount: 589340,
  commentsCount: 266112,
  sharesCount: 583615,
  postUrn: "<value>",
  postId: "<id>",
  type: "activity",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `text`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `date`                                                                                                    | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `likesCount`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `commentsCount`                                                                                           | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `sharesCount`                                                                                             | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `postUrn`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `postId`                                                                                                  | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `type`                                                                                                    | [operations.RefreshMyLinkedInProfileType](../../models/operations/refresh-my-linked-in-profile-type.md)   | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `media`                                                                                                   | [operations.RefreshMyLinkedInProfileMedia](../../models/operations/refresh-my-linked-in-profile-media.md) | :heavy_minus_sign:                                                                                        | Media attached to the post (image, video, document, or article). Absent when the post is text-only.       |