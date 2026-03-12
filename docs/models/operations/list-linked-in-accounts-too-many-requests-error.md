# ListLinkedInAccountsTooManyRequestsError

## Example Usage

```typescript
import { ListLinkedInAccountsTooManyRequestsError } from "bereach/models/operations";

let value: ListLinkedInAccountsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 292772,
  daily: {
    current: 362217,
    limit: 852057,
  },
  weekly: {
    current: 680590,
    limit: 18202,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.ListLinkedInAccountsCode](../../models/operations/list-linked-in-accounts-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.ListLinkedInAccountsDaily](../../models/operations/list-linked-in-accounts-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.ListLinkedInAccountsWeekly](../../models/operations/list-linked-in-accounts-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |