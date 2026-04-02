# Appearances

## Example Usage

```typescript
import { Appearances } from "bereach/models/operations";

let value: Appearances = {
  count: 367328,
  keywords: [
    "<value 1>",
    "<value 2>",
  ],
  companies: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `count`                                             | *number*                                            | :heavy_check_mark:                                  | N/A                                                 |
| `keywords`                                          | *any*[]                                             | :heavy_check_mark:                                  | Top search keywords that led to your profile        |
| `companies`                                         | *any*[]                                             | :heavy_check_mark:                                  | Companies of people who found you                   |
| `raw`                                               | *any*                                               | :heavy_minus_sign:                                  | Raw LinkedIn API response (included when available) |