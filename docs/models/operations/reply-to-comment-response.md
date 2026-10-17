# ReplyToCommentResponse

Reply sent successfully

## Example Usage

```typescript
import { ReplyToCommentResponse } from "bereach/models/operations";

let value: ReplyToCommentResponse = {
  success: true,
  creditsUsed: 515931,
  retryAfter: 153833,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `replyUrn`                                                                                                                                | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | URN of the created reply comment                                                                                                          |
| `duplicate`                                                                                                                               | *boolean*                                                                                                                                 | :heavy_minus_sign:                                                                                                                        | True if this action was already executed for the given campaignSlug + target.                                                             |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ReplyToCommentMeta](../../models/operations/reply-to-comment-meta.md)                                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |