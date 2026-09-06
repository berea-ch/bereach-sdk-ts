# EditCommentMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { EditCommentMeta } from "bereach/models/operations";

let value: EditCommentMeta = {
  credits: {
    current: 5879.73,
    limit: 3635.76,
    remaining: 3272.22,
    percentage: 4052.69,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.EditCommentCredits](../../models/operations/edit-comment-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |