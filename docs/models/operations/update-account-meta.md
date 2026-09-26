# UpdateAccountMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UpdateAccountMeta } from "bereach/models/operations";

let value: UpdateAccountMeta = {
  credits: {
    current: 5023.89,
    limit: 1450.04,
    remaining: 8663.42,
    percentage: 5378.61,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.UpdateAccountCredits](../../models/operations/update-account-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |