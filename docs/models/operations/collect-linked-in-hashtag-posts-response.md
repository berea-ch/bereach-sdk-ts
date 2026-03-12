# CollectLinkedInHashtagPostsResponse

Hashtag posts

## Example Usage

```typescript
import { CollectLinkedInHashtagPostsResponse } from "bereach/models/operations";

let value: CollectLinkedInHashtagPostsResponse = {
  success: true,
  posts: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  creditsUsed: 359767,
  retryAfter: 949674,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | *any*[]                                                                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |