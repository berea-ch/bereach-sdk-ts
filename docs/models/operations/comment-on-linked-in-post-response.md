# CommentOnLinkedInPostResponse

Comment posted successfully

## Example Usage

```typescript
import { CommentOnLinkedInPostResponse } from "bereach/models/operations";

let value: CommentOnLinkedInPostResponse = {
  success: true,
  creditsUsed: 189155,
  retryAfter: 885584,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `commentUrn`                                                                         | *string*                                                                             | :heavy_minus_sign:                                                                   | URN of the created comment (e.g., 'urn:li:comment:(activity:PARENT_ID,COMMENT_ID)')  |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | True if this action was already executed for the given campaignSlug + target.        |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |