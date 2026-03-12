# CollectLinkedInCommentRepliesResponse

List of replies to the comment

## Example Usage

```typescript
import { CollectLinkedInCommentRepliesResponse } from "bereach/models/operations";

let value: CollectLinkedInCommentRepliesResponse = {
  success: true,
  replies: [
    {
      name: "<value>",
      headline: "<value>",
      profileUrl: "https://shimmering-finer.com",
      imageUrl: "https://assured-mountain.com/",
      type: "comment",
      timestamp: 928156,
      knownDistance: 632615,
    },
  ],
  count: 661519,
  total: 746735,
  start: 388666,
  hasMore: true,
  parentCommentUrn: "<value>",
  previousTotal: 951747,
  creditsUsed: 137926,
  retryAfter: 971878,
};
```

## Fields

| Field                                                                                                                                                            | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                        | *true*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `replies`                                                                                                                                                        | [operations.Reply](../../models/operations/reply.md)[]                                                                                                           | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `count`                                                                                                                                                          | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `total`                                                                                                                                                          | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `start`                                                                                                                                                          | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `hasMore`                                                                                                                                                        | *boolean*                                                                                                                                                        | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `parentCommentUrn`                                                                                                                                               | *string*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `previousTotal`                                                                                                                                                  | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The total from your last call to this endpoint for the same comment (null on first call). Compare with total to detect new replies without client-side tracking. |
| `creditsUsed`                                                                                                                                                    | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                                                             |
| `retryAfter`                                                                                                                                                     | *number*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | Seconds to wait before making another call of the same type. 0 means no wait needed.                                                                             |