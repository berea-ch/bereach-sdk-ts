# SaveLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { SaveLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: SaveLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 680944,
  daily: {
    current: 580166,
    limit: 115692,
  },
  weekly: {
    current: 525648,
    limit: 475956,
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `code`                                                                                     | [operations.SaveLinkedInPostCode](../../models/operations/save-linked-in-post-code.md)     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `message`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `docs`                                                                                     | *string*                                                                                   | :heavy_minus_sign:                                                                         | N/A                                                                                        |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before retrying.                                                           |
| `daily`                                                                                    | [operations.SaveLinkedInPostDaily](../../models/operations/save-linked-in-post-daily.md)   | :heavy_check_mark:                                                                         | Current and max daily usage (null if no daily cap).                                        |
| `weekly`                                                                                   | [operations.SaveLinkedInPostWeekly](../../models/operations/save-linked-in-post-weekly.md) | :heavy_check_mark:                                                                         | Current and max weekly usage (null if no weekly cap).                                      |