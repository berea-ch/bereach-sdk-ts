# ListSalesNavFiltersMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListSalesNavFiltersMeta } from "bereach/models/operations";

let value: ListSalesNavFiltersMeta = {
  credits: {
    current: 3160.94,
    limit: 4571.66,
    remaining: 134.29,
    percentage: 7164.22,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `credits`                                                                                          | [operations.ListSalesNavFiltersCredits](../../models/operations/list-sales-nav-filters-credits.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |