# GetFollowersResponse

Paginated list of followers

## Example Usage

```typescript
import { GetFollowersResponse } from "bereach/models/operations";

let value: GetFollowersResponse = {
  success: true,
  followers: [
    {
      name: "<value>",
      headline: "<value>",
      profileUrl: "https://illiterate-reboot.org/",
      profilePicture: "<value>",
      followerCount: 141489,
      following: true,
      profileUrn: "<value>",
      publicIdentifier: "<value>",
    },
  ],
  count: 105256,
  totalFollowers: 861151,
  start: 273490,
  hasMore: true,
  creditsUsed: 228643,
  retryAfter: 488184,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `followers`                                                                          | [operations.Follower](../../models/operations/follower.md)[]                         | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `count`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `totalFollowers`                                                                     | *number*                                                                             | :heavy_check_mark:                                                                   | Total reported by LinkedIn (capped at ~1000)                                         |
| `start`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |