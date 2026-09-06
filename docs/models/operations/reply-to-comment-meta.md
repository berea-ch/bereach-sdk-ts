# ReplyToCommentMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ReplyToCommentMeta } from "bereach/models/operations";

let value: ReplyToCommentMeta = {
  credits: {
    current: 3282.95,
    limit: 7220.5,
    remaining: 2996.08,
    percentage: 4434.97,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `credits`                                                                               | [operations.ReplyToCommentCredits](../../models/operations/reply-to-comment-credits.md) | :heavy_check_mark:                                                                      | N/A                                                                                     |