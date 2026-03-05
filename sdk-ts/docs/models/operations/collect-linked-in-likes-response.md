# CollectLinkedInLikesResponse

List of profiles who liked the post

## Example Usage

```typescript
import { CollectLinkedInLikesResponse } from "bereach/models/operations";

let value: CollectLinkedInLikesResponse = {
  success: true,
  profiles: [
    {
      name: "<value>",
      headline: "<value>",
      profileUrl: "https://jaunty-bar.org/",
      imageUrl: "https://remorseful-footrest.net",
      type: "like",
    },
  ],
  count: 107854,
  total: 179138,
  start: 664937,
  hasMore: false,
  previousTotal: 612117,
  creditsUsed: 964493,
  retryAfter: 514702,
};
```

## Fields

| Field                                                                                                                                                       | Type                                                                                                                                                        | Required                                                                                                                                                    | Description                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                   | *boolean*                                                                                                                                                   | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `profiles`                                                                                                                                                  | [operations.CollectLinkedInLikesProfile](../../models/operations/collect-linked-in-likes-profile.md)[]                                                      | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `count`                                                                                                                                                     | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `total`                                                                                                                                                     | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `start`                                                                                                                                                     | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `hasMore`                                                                                                                                                   | *boolean*                                                                                                                                                   | :heavy_check_mark:                                                                                                                                          | N/A                                                                                                                                                         |
| `previousTotal`                                                                                                                                             | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | The total from your last call to this endpoint for the same post (null on first call). Compare with total to detect new likes without client-side tracking. |
| `creditsUsed`                                                                                                                                               | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                                                        |
| `retryAfter`                                                                                                                                                | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | Seconds to wait before making another call of the same type. 0 means no wait needed.                                                                        |