# GetFeedResponse

Feed posts

## Example Usage

```typescript
import { GetFeedResponse } from "bereach/models/operations";

let value: GetFeedResponse = {
  success: true,
  posts: [],
  creditsUsed: 654400,
  retryAfter: 814602,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | [operations.GetFeedPost](../../models/operations/get-feed-post.md)[]                 | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |