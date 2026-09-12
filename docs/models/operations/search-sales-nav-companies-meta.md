# SearchSalesNavCompaniesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchSalesNavCompaniesMeta } from "bereach/models/operations";

let value: SearchSalesNavCompaniesMeta = {
  credits: {
    current: 2868.32,
    limit: 2464.65,
    remaining: 2515.9,
    percentage: 1146.42,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                                  | [operations.SearchSalesNavCompaniesCredits](../../models/operations/search-sales-nav-companies-credits.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |