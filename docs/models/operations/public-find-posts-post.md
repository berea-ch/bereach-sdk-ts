# PublicFindPostsPost

## Example Usage

```typescript
import { PublicFindPostsPost } from "bereach/models/operations";

let value: PublicFindPostsPost = {
  url: "https://elegant-statue.net/",
  text: "<value>",
  author: "<value>",
  authorName: null,
  authorHeadline: "<value>",
  publishedAt: "<value>",
};
```

## Fields

| Field                                                                                                                                             | Type                                                                                                                                              | Required                                                                                                                                          | Description                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `url`                                                                                                                                             | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | N/A                                                                                                                                               |
| `text`                                                                                                                                            | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | N/A                                                                                                                                               |
| `author`                                                                                                                                          | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | The publisher's vanity identifier, read off the post URL. An identifier, not a display name, and some belong to company pages rather than people. |
| `authorName`                                                                                                                                      | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | The publisher's display name, when the post carried one. Null when it did not.                                                                    |
| `authorHeadline`                                                                                                                                  | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | The publisher's headline, when the post carried one. Null when it did not.                                                                        |
| `publishedAt`                                                                                                                                     | *string*                                                                                                                                          | :heavy_check_mark:                                                                                                                                | When the post was published, ISO 8601. Null when it is not known.                                                                                 |