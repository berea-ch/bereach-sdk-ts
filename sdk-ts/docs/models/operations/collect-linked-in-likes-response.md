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
      type: "like",
    },
  ],
  count: 686642,
  total: 854826,
  start: 487665,
  hasMore: true,
  previousTotal: null,
  creditsUsed: 924518,
  retryAfter: 967238,
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