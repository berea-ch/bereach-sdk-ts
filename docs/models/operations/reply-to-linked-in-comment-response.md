# ReplyToLinkedInCommentResponse

Reply sent successfully

## Example Usage

```typescript
import { ReplyToLinkedInCommentResponse } from "bereach/models/operations";

let value: ReplyToLinkedInCommentResponse = {
  success: true,
  creditsUsed: 208821,
  retryAfter: 683276,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `replyUrn`                                                                           | *string*                                                                             | :heavy_minus_sign:                                                                   | URN of the created reply comment                                                     |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | True if this action was already executed for the given campaignSlug + target.        |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |