# ListSalesNavSavedSearchesSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ListSalesNavSavedSearchesSpent } from "bereach/models/operations";

let value: ListSalesNavSavedSearchesSpent = {
  amount: 1835.14,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                          | *number*                                                                                                          | :heavy_check_mark:                                                                                                | The money spent.                                                                                                  |
| `currency`                                                                                                        | [operations.ListSalesNavSavedSearchesCurrency](../../models/operations/list-sales-nav-saved-searches-currency.md) | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `text`                                                                                                            | *string*                                                                                                          | :heavy_check_mark:                                                                                                | The amount as a person reads it, with its currency.                                                               |