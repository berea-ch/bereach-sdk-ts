# CollectSavedLinkedInPostsResponse

Saved posts

## Example Usage

```typescript
import { CollectSavedLinkedInPostsResponse } from "bereach/models/operations";

let value: CollectSavedLinkedInPostsResponse = {
  success: true,
  posts: [
    "<value 1>",
  ],
  total: 187413,
  creditsUsed: 888175,
  retryAfter: 214138,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `posts`                                                                              | *any*[]                                                                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |