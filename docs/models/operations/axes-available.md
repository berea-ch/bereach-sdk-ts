# AxesAvailable

## Example Usage

```typescript
import { AxesAvailable } from "bereach/models/operations";

let value: AxesAvailable = {
  axis: "<value>",
  queries: 810573,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `axis`                                                                 | *string*                                                               | :heavy_check_mark:                                                     | A search angle this audience supports, e.g. title, city, school, tool. |
| `queries`                                                              | *number*                                                               | :heavy_check_mark:                                                     | How many searches that angle could run in total.                       |