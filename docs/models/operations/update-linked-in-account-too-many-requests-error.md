# UpdateLinkedInAccountTooManyRequestsError

## Example Usage

```typescript
import { UpdateLinkedInAccountTooManyRequestsError } from "bereach/models/operations";

let value: UpdateLinkedInAccountTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 509933,
  daily: {
    current: 383337,
    limit: 74437,
  },
  weekly: {
    current: 965237,
    limit: 496678,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `code`                                                                                               | [operations.UpdateLinkedInAccountCode](../../models/operations/update-linked-in-account-code.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `message`                                                                                            | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `docs`                                                                                               | *string*                                                                                             | :heavy_minus_sign:                                                                                   | N/A                                                                                                  |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before retrying.                                                                     |
| `daily`                                                                                              | [operations.UpdateLinkedInAccountDaily](../../models/operations/update-linked-in-account-daily.md)   | :heavy_check_mark:                                                                                   | Current and max daily usage (null if no daily cap).                                                  |
| `weekly`                                                                                             | [operations.UpdateLinkedInAccountWeekly](../../models/operations/update-linked-in-account-weekly.md) | :heavy_check_mark:                                                                                   | Current and max weekly usage (null if no weekly cap).                                                |