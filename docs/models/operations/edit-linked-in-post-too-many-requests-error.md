# EditLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { EditLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: EditLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 144467,
  daily: {
    current: 451456,
    limit: 811,
  },
  weekly: {
    current: 482546,
    limit: 871991,
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `code`                                                                                     | [operations.EditLinkedInPostCode](../../models/operations/edit-linked-in-post-code.md)     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `message`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `docs`                                                                                     | *string*                                                                                   | :heavy_minus_sign:                                                                         | N/A                                                                                        |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before retrying.                                                           |
| `daily`                                                                                    | [operations.EditLinkedInPostDaily](../../models/operations/edit-linked-in-post-daily.md)   | :heavy_check_mark:                                                                         | Current and max daily usage (null if no daily cap).                                        |
| `weekly`                                                                                   | [operations.EditLinkedInPostWeekly](../../models/operations/edit-linked-in-post-weekly.md) | :heavy_check_mark:                                                                         | Current and max weekly usage (null if no weekly cap).                                      |