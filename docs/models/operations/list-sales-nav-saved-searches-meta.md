# ListSalesNavSavedSearchesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListSalesNavSavedSearchesMeta } from "bereach/models/operations";

let value: ListSalesNavSavedSearchesMeta = {
  credits: {
    current: 4062.1,
    limit: 2972.85,
    remaining: 3841.55,
    percentage: 936.22,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                                       | [operations.ListSalesNavSavedSearchesCredits](../../models/operations/list-sales-nav-saved-searches-credits.md) | :heavy_check_mark:                                                                                              | N/A                                                                                                             |