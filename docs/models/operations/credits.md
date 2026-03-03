# Credits

## Example Usage

```typescript
import { Credits } from "bereach/models/operations";

let value: Credits = {
  current: 683894,
  limit: 620960,
  remaining: 290864,
  percentage: 8034.06,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `current`                                                       | *number*                                                        | :heavy_check_mark:                                              | Number of credits used in the current billing period            |
| `limit`                                                         | *number*                                                        | :heavy_check_mark:                                              | Maximum credits available for the workspace                     |
| `remaining`                                                     | *number*                                                        | :heavy_check_mark:                                              | Credits remaining before hitting the limit                      |
| `percentage`                                                    | *number*                                                        | :heavy_check_mark:                                              | Percentage of credits used (0-100, rounded to 2 decimal places) |