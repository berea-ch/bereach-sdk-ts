# AxesTried

## Example Usage

```typescript
import { AxesTried } from "bereach/models/operations";

let value: AxesTried = {
  axis: "<value>",
  queriesPlanned: 156145,
  attempted: 725063,
  yielded: 130260,
  exhausted: false,
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `axis`                                                              | *string*                                                            | :heavy_check_mark:                                                  | Which search angle this row covers, e.g. title, city, school, tool. |
| `queriesPlanned`                                                    | *number*                                                            | :heavy_check_mark:                                                  | How many searches this angle could run in total.                    |
| `attempted`                                                         | *number*                                                            | :heavy_check_mark:                                                  | How many of those have actually run so far.                         |
| `yielded`                                                           | *number*                                                            | :heavy_check_mark:                                                  | New people this angle has contributed.                              |
| `exhausted`                                                         | *boolean*                                                           | :heavy_check_mark:                                                  | Whether this angle has nothing left to try.                         |