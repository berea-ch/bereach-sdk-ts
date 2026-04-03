# GetCreditsCredits

## Example Usage

```typescript
import { GetCreditsCredits } from "bereach/models/operations";

let value: GetCreditsCredits = {
  current: 318947,
  limit: 71114,
  remaining: null,
  percentage: 3198.98,
  isUnlimited: true,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `current`                                                                                        | *number*                                                                                         | :heavy_check_mark:                                                                               | Number of credits used in the current billing period                                             |
| `limit`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | Maximum credits available for the workspace, or null if unlimited                                |
| `remaining`                                                                                      | *number*                                                                                         | :heavy_check_mark:                                                                               | Credits remaining before hitting the limit, or null if unlimited                                 |
| `percentage`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Percentage of credits used (0-100, capped at 100, rounded to 2 decimal places). 0 when unlimited |
| `isUnlimited`                                                                                    | *boolean*                                                                                        | :heavy_check_mark:                                                                               | Whether the workspace has unlimited credits (Pro plan). When true, limit and remaining are null  |