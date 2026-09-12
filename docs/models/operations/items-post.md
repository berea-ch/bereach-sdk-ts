# ItemsPost

## Example Usage

```typescript
import { ItemsPost } from "bereach/models/operations";

let value: ItemsPost = {
  postUrl: "https://elegant-pear.name/",
  text: "<value>",
  date: 76696,
  likesCount: 39647,
  commentsCount: 495127,
  sharesCount: 992575,
  postUrn: "<value>",
  postId: "<id>",
  type: "POST",
  author: {
    name: "<value>",
    profileUrl: "https://low-cap.org/",
    headline: null,
    profilePicture: "<value>",
    isCompany: true,
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  isRepost: true,
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | Public URL of the post.                                                                                   |
| `text`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | Post text content.                                                                                        |
| `date`                                                                                                    | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Post creation timestamp (Unix milliseconds).                                                              |
| `likesCount`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Total reactions on this post.                                                                             |
| `commentsCount`                                                                                           | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Total top-level comments on this post.                                                                    |
| `sharesCount`                                                                                             | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Total shares/reposts of this post.                                                                        |
| `postUrn`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | LinkedIn internal URN for this post. Use with engagement tools (like, comment, collect_engagers).         |
| `postId`                                                                                                  | *string*                                                                                                  | :heavy_check_mark:                                                                                        | Numeric post identifier parsed from the URN.                                                              |
| `media`                                                                                                   | [operations.SearchByUrlMedia](../../models/operations/search-by-url-media.md)                             | :heavy_minus_sign:                                                                                        | Media attached to the post (image, video, document, or article). Absent when the post is text-only.       |
| `repostedFromName`                                                                                        | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | On a repost, the ORIGINAL author's name when it differs from the resharer.                                |
| `reactionTypeCounts`                                                                                      | [operations.SearchByUrlReactionTypeCount](../../models/operations/search-by-url-reaction-type-count.md)[] | :heavy_minus_sign:                                                                                        | Per-reaction-type breakdown, when LinkedIn exposes it.                                                    |
| `numImpressions`                                                                                          | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | Total impressions, exposed only on Creator-mode posts.                                                    |
| `highlightedReactorName`                                                                                  | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | Social-proof attribution, when LinkedIn surfaces one in the feed.                                         |
| `viewerLiked`                                                                                             | *boolean*                                                                                                 | :heavy_minus_sign:                                                                                        | Whether the authenticated account has reacted to this post.                                               |
| `type`                                                                                                    | [operations.SearchByUrlTypePost](../../models/operations/search-by-url-type-post.md)                      | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `author`                                                                                                  | [operations.SearchByUrlAuthor](../../models/operations/search-by-url-author.md)                           | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `isRepost`                                                                                                | *boolean*                                                                                                 | :heavy_check_mark:                                                                                        | N/A                                                                                                       |