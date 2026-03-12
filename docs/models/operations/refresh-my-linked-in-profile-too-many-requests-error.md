# RefreshMyLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { RefreshMyLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: RefreshMyLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 613327,
  daily: {
    current: 846965,
    limit: 484850,
  },
  weekly: {
    current: 931167,
    limit: 292044,
  },
};
```

## Fields

| Field                                                                                                       | Type                                                                                                        | Required                                                                                                    | Description                                                                                                 |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                      | [operations.RefreshMyLinkedInProfileCode](../../models/operations/refresh-my-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `message`                                                                                                   | *string*                                                                                                    | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `docs`                                                                                                      | *string*                                                                                                    | :heavy_minus_sign:                                                                                          | N/A                                                                                                         |
| `retryAfter`                                                                                                | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Seconds to wait before retrying.                                                                            |
| `daily`                                                                                                     | [operations.RefreshMyLinkedInProfileDaily](../../models/operations/refresh-my-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                          | Current and max daily usage (null if no daily cap).                                                         |
| `weekly`                                                                                                    | [operations.RefreshMyLinkedInProfileWeekly](../../models/operations/refresh-my-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                          | Current and max weekly usage (null if no weekly cap).                                                       |