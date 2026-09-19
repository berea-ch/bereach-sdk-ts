# SearchSalesNavMeta2

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchSalesNavMeta2 } from "bereach/models/operations";

let value: SearchSalesNavMeta2 = {
  credits: {
    current: 1018.84,
    limit: 8827.21,
    remaining: 5069.36,
    percentage: 4199.57,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `credits`                                                                                 | [operations.SearchSalesNavCredits2](../../models/operations/search-sales-nav-credits2.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |