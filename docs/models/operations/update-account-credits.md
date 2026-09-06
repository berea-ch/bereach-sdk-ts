# UpdateAccountCredits

## Example Usage

```typescript
import { UpdateAccountCredits } from "bereach/models/operations";

let value: UpdateAccountCredits = {
  current: 5019.75,
  limit: null,
  remaining: 1429.56,
  percentage: 2349,
  isUnlimited: false,
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