# ListSalesNavFiltersSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ListSalesNavFiltersSpent } from "bereach/models/operations";

let value: ListSalesNavFiltersSpent = {
  amount: 8720.39,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `amount`                                                                                             | *number*                                                                                             | :heavy_check_mark:                                                                                   | The money spent.                                                                                     |
| `currency`                                                                                           | [operations.ListSalesNavFiltersCurrency](../../models/operations/list-sales-nav-filters-currency.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `text`                                                                                               | *string*                                                                                             | :heavy_check_mark:                                                                                   | The amount as a person reads it, with its currency.                                                  |