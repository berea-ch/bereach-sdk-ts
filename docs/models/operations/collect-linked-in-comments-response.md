# CollectLinkedInCommentsResponse

List of profiles who commented on the post

## Example Usage

```typescript
import { CollectLinkedInCommentsResponse } from "bereach/models/operations";

let value: CollectLinkedInCommentsResponse = {
  success: true,
  profiles: [
    {
      name: "<value>",
      headline: "<value>",
      profileUrl: "https://winged-term.biz",
      imageUrl: "https://neighboring-tuba.biz",
      type: "comment",
      timestamp: 549293,
      knownDistance: 242256,
    },
  ],
  count: 563108,
  total: 89619,
  start: 526427,
  hasMore: true,
  previousTotal: 701385,
  creditsUsed: 4313,
  retryAfter: 143921,
};
```

## Fields

| Field                                                                                                                                                          | Type                                                                                                                                                           | Required                                                                                                                                                       | Description                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                      | *true*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `profiles`                                                                                                                                                     | [operations.CollectLinkedInCommentsProfile](../../models/operations/collect-linked-in-comments-profile.md)[]                                                   | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `count`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `total`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `start`                                                                                                                                                        | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `hasMore`                                                                                                                                                      | *boolean*                                                                                                                                                      | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `previousTotal`                                                                                                                                                | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | The total from your last call to this endpoint for the same post (null on first call). Compare with total to detect new comments without client-side tracking. |
| `processedCount`                                                                                                                                               | *number*                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                             | Number of returned profiles that already have a completed 'message' action in this campaign. Only present when campaignSlug is provided.                       |
| `newCount`                                                                                                                                                     | *number*                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                             | Number of returned profiles that have NOT yet been messaged in this campaign. Only present when campaignSlug is provided.                                      |
| `creditsUsed`                                                                                                                                                  | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                                                           |
| `retryAfter`                                                                                                                                                   | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Seconds to wait before making another call of the same type. 0 means no wait needed.                                                                           |