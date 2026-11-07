# GetOwnActivitySpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { GetOwnActivitySpent } from "bereach/models/operations";

let value: GetOwnActivitySpent = {
  amount: 3731.32,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `amount`                                                                                  | *number*                                                                                  | :heavy_check_mark:                                                                        | The money spent.                                                                          |
| `currency`                                                                                | [operations.GetOwnActivityCurrency](../../models/operations/get-own-activity-currency.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `text`                                                                                    | *string*                                                                                  | :heavy_check_mark:                                                                        | The amount as a person reads it, with its currency.                                       |