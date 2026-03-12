# VisitLinkedInCompanyTooManyRequestsError

## Example Usage

```typescript
import { VisitLinkedInCompanyTooManyRequestsError } from "bereach/models/operations";

let value: VisitLinkedInCompanyTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 568800,
  daily: {
    current: 69667,
    limit: 191048,
  },
  weekly: {
    current: 863453,
    limit: 527691,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.VisitLinkedInCompanyCode](../../models/operations/visit-linked-in-company-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.VisitLinkedInCompanyDaily](../../models/operations/visit-linked-in-company-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.VisitLinkedInCompanyWeekly](../../models/operations/visit-linked-in-company-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |