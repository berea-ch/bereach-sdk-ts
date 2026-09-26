# CollectPostsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CollectPostsMeta } from "bereach/models/operations";

let value: CollectPostsMeta = {
  credits: {
    current: 8930.14,
    limit: 2754.5,
    remaining: 9024.95,
    percentage: 4345.42,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.CollectPostsCredits](../../models/operations/collect-posts-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |