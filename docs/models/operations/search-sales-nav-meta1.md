# SearchSalesNavMeta1

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchSalesNavMeta1 } from "bereach/models/operations";

let value: SearchSalesNavMeta1 = {
  credits: {
    current: 6295.43,
    limit: 8881.47,
    remaining: 8632.6,
    percentage: 9411.13,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `credits`                                                                                 | [operations.SearchSalesNavCredits1](../../models/operations/search-sales-nav-credits1.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |