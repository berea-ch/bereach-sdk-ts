# GetConnectionStatusCredits

## Example Usage

```typescript
import { GetConnectionStatusCredits } from "bereach/models/operations";

let value: GetConnectionStatusCredits = {
  current: 6356.68,
  limit: 263.89,
  remaining: 8362.96,
  percentage: 4044.14,
  isUnlimited: true,
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `current`                                 | *number*                                  | :heavy_check_mark:                        | Credits spent this period.                |
| `limit`                                   | *number*                                  | :heavy_check_mark:                        | Period allowance, or null when unlimited. |
| `remaining`                               | *number*                                  | :heavy_check_mark:                        | Allowance left, or null when unlimited.   |
| `percentage`                              | *number*                                  | :heavy_check_mark:                        | Share of the allowance spent, 0 to 100.   |
| `isUnlimited`                             | *boolean*                                 | :heavy_check_mark:                        | N/A                                       |