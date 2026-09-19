# DeleteCommentMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { DeleteCommentMeta } from "bereach/models/operations";

let value: DeleteCommentMeta = {
  credits: {
    current: 4603.15,
    limit: 8438.05,
    remaining: 3107.74,
    percentage: 1234.51,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.DeleteCommentCredits](../../models/operations/delete-comment-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |