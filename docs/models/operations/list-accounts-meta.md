# ListAccountsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListAccountsMeta } from "bereach/models/operations";

let value: ListAccountsMeta = {
  credits: {
    current: 5037.93,
    limit: null,
    remaining: 1564.94,
    percentage: 1638.74,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.ListAccountsCredits](../../models/operations/list-accounts-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |