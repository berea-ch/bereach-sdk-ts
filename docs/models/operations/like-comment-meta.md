# LikeCommentMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { LikeCommentMeta } from "bereach/models/operations";

let value: LikeCommentMeta = {
  credits: {
    current: 6557.71,
    limit: 4839.46,
    remaining: 1447.33,
    percentage: 2093.88,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.LikeCommentCredits](../../models/operations/like-comment-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |