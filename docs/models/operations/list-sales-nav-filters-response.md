# ListSalesNavFiltersResponse

Available Sales Nav filters for this seat.

## Example Usage

```typescript
import { ListSalesNavFiltersResponse } from "bereach/models/operations";

let value: ListSalesNavFiltersResponse = {
  success: true,
  filters: [
    {
      name: "<value>",
      field: "<value>",
      group: "<value>",
      valueKind: "enum",
      supportsExclude: false,
      available: true,
    },
  ],
  count: 190581,
  creditsUsed: 685248,
  retryAfter: 318980,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `filters`                                                                                                                                 | [operations.Filter](../../models/operations/filter.md)[]                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ListSalesNavFiltersMeta](../../models/operations/list-sales-nav-filters-meta.md)                                              | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |