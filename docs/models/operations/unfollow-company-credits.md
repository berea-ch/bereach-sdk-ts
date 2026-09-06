# UnfollowCompanyCredits

## Example Usage

```typescript
import { UnfollowCompanyCredits } from "bereach/models/operations";

let value: UnfollowCompanyCredits = {
  current: 152.98,
  limit: 5128.3,
  remaining: 3912.95,
  percentage: 5956.51,
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