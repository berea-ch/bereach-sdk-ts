# DeleteCommentResponse

Comment deleted (or already gone)

## Example Usage

```typescript
import { DeleteCommentResponse } from "bereach/models/operations";

let value: DeleteCommentResponse = {
  success: true,
  deleted: {
    type: "ugcPost",
    parentId: "<id>",
    commentId: "<id>",
    alreadyGone: true,
  },
  creditsUsed: 738118,
  retryAfter: 348925,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `deleted`                                                                                                                                 | [operations.Deleted](../../models/operations/deleted.md)                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.DeleteCommentMeta](../../models/operations/delete-comment-meta.md)                                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |