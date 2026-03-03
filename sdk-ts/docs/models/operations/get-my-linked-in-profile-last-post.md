# GetMyLinkedInProfileLastPost

## Example Usage

```typescript
import { GetMyLinkedInProfileLastPost } from "bereach/models/operations";

let value: GetMyLinkedInProfileLastPost = {
  postUrl: "https://gummy-impact.com/",
  text: "<value>",
  date: 971043,
  likesCount: 449500,
  commentsCount: 583939,
  sharesCount: 427665,
  postUrn: "<value>",
  postId: "<id>",
  type: "share",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `text`                                                                                          | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `date`                                                                                          | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `likesCount`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `commentsCount`                                                                                 | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `sharesCount`                                                                                   | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `postUrn`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `postId`                                                                                        | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `type`                                                                                          | [operations.GetMyLinkedInProfileType](../../models/operations/get-my-linked-in-profile-type.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |