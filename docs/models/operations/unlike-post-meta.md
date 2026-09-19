# UnlikePostMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UnlikePostMeta } from "bereach/models/operations";

let value: UnlikePostMeta = {
  credits: {
    current: 821.7,
    limit: 4601.74,
    remaining: 6905.71,
    percentage: 9068.32,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `credits`                                                                      | [operations.UnlikePostCredits](../../models/operations/unlike-post-credits.md) | :heavy_check_mark:                                                             | N/A                                                                            |