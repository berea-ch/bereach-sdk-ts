# UnlikeCommentMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UnlikeCommentMeta } from "bereach/models/operations";

let value: UnlikeCommentMeta = {
  credits: {
    current: 2171.02,
    limit: 3771.08,
    remaining: 7700.97,
    percentage: 9561.23,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.UnlikeCommentCredits](../../models/operations/unlike-comment-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |