# AcceptInvitationCredits

## Example Usage

```typescript
import { AcceptInvitationCredits } from "bereach/models/operations";

let value: AcceptInvitationCredits = {
  current: 5117.75,
  limit: 3063.5,
  remaining: 5973.93,
  percentage: 3152.83,
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