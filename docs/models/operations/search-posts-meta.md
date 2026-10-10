# SearchPostsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchPostsMeta } from "bereach/models/operations";

let value: SearchPostsMeta = {
  credits: {
    current: 6597.78,
    limit: null,
    remaining: 8277.51,
    percentage: 3044.68,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.SearchPostsCredits](../../models/operations/search-posts-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |