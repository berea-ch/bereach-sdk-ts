# GetMyLimitsTooManyRequestsError

## Example Usage

```typescript
import { GetMyLimitsTooManyRequestsError } from "bereach/models/operations";

let value: GetMyLimitsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 23194,
  daily: {
    current: 852161,
    limit: 282293,
  },
  weekly: {
    current: 638076,
    limit: 520031,
  },
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                           | [operations.GetMyLimitsCode](../../models/operations/get-my-limits-code.md)                                      | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `message`                                                                                                        | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `docs`                                                                                                           | *string*                                                                                                         | :heavy_minus_sign:                                                                                               | N/A                                                                                                              |
| `retryAfter`                                                                                                     | *number*                                                                                                         | :heavy_check_mark:                                                                                               | Seconds to wait before retrying.                                                                                 |
| `daily`                                                                                                          | [operations.GetMyLimitsTooManyRequestsDaily](../../models/operations/get-my-limits-too-many-requests-daily.md)   | :heavy_check_mark:                                                                                               | Current and max daily usage (null if no daily cap).                                                              |
| `weekly`                                                                                                         | [operations.GetMyLimitsTooManyRequestsWeekly](../../models/operations/get-my-limits-too-many-requests-weekly.md) | :heavy_check_mark:                                                                                               | Current and max weekly usage (null if no weekly cap).                                                            |