# LikeLinkedInCommentResponse

Comment liked successfully

## Example Usage

```typescript
import { LikeLinkedInCommentResponse } from "bereach/models/operations";

let value: LikeLinkedInCommentResponse = {
  success: false,
  creditsUsed: 464019,
  retryAfter: 41362,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `resourceKey`                                                                        | *string*                                                                             | :heavy_minus_sign:                                                                   | Resource key of the created reaction                                                 |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | True if this action was already executed for the given campaignSlug + target.        |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |