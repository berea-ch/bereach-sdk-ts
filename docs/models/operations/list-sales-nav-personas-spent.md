# ListSalesNavPersonasSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ListSalesNavPersonasSpent } from "bereach/models/operations";

let value: ListSalesNavPersonasSpent = {
  amount: 4594.09,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                               | *number*                                                                                               | :heavy_check_mark:                                                                                     | The money spent.                                                                                       |
| `currency`                                                                                             | [operations.ListSalesNavPersonasCurrency](../../models/operations/list-sales-nav-personas-currency.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `text`                                                                                                 | *string*                                                                                               | :heavy_check_mark:                                                                                     | The amount as a person reads it, with its currency.                                                    |