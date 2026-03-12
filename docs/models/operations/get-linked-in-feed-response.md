# GetLinkedInFeedResponse

Feed posts

## Example Usage

```typescript
import { GetLinkedInFeedResponse } from "bereach/models/operations";

let value: GetLinkedInFeedResponse = {
  success: true,
  posts: [
    "<value 1>",
    "<value 2>",
  ],
  creditsUsed: 264746,
  retryAfter: 117961,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | *any*[]                                                                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |