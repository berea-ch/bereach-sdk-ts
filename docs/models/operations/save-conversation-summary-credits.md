# SaveConversationSummaryCredits

## Example Usage

```typescript
import { SaveConversationSummaryCredits } from "bereach/models/operations";

let value: SaveConversationSummaryCredits = {
  current: 2896.1,
  limit: 9478.57,
  remaining: null,
  percentage: 9465.1,
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