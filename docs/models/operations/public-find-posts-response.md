# PublicFindPostsResponse

Matched posts

## Example Usage

```typescript
import { PublicFindPostsResponse } from "bereach/models/operations";

let value: PublicFindPostsResponse = {
  source: "public",
  provider: "<value>",
  query: "<value>",
  posts: [],
  moreAvailable: false,
};
```

## Fields

| Field                                                                                                                                         | Type                                                                                                                                          | Required                                                                                                                                      | Description                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `source`                                                                                                                                      | [operations.PublicFindPostsSource](../../models/operations/public-find-posts-source.md)                                                       | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `provider`                                                                                                                                    | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The search provider that answered.                                                                                                            |
| `query`                                                                                                                                       | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The exact query sent, so a thin result set can be read rather than guessed at.                                                                |
| `posts`                                                                                                                                       | [operations.PublicFindPostsPost](../../models/operations/public-find-posts-post.md)[]                                                         | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `moreAvailable`                                                                                                                               | *boolean*                                                                                                                                     | :heavy_check_mark:                                                                                                                            | Whether asking again with more can still reach rows you have not seen. False means this ask is walked out; say so and do not call more again. |
| `duplicates`                                                                                                                                  | *number*                                                                                                                                      | :heavy_minus_sign:                                                                                                                            | Rows a continuation re-reached and dropped as already delivered. Normal bookkeeping, never a failure.                                         |