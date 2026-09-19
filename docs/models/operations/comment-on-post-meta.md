# CommentOnPostMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CommentOnPostMeta } from "bereach/models/operations";

let value: CommentOnPostMeta = {
  credits: {
    current: 5556.41,
    limit: 3496.92,
    remaining: 4899.53,
    percentage: 5509.89,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `credits`                                                                             | [operations.CommentOnPostCredits](../../models/operations/comment-on-post-credits.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |