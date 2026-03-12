# VisitLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { VisitLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: VisitLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 59124,
  daily: {
    current: 951341,
    limit: 736762,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.VisitLinkedInProfileCode](../../models/operations/visit-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.VisitLinkedInProfileDaily](../../models/operations/visit-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.VisitLinkedInProfileWeekly](../../models/operations/visit-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |