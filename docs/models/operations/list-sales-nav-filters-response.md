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

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `filters`                                                                                                                            | [operations.Filter](../../models/operations/filter.md)[]                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `count`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ListSalesNavFiltersSpent](../../models/operations/list-sales-nav-filters-spent.md)                                       | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |