# GetMyLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { GetMyLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: GetMyLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 852622,
  daily: {
    current: 747399,
    limit: 863220,
  },
  weekly: {
    current: 696254,
    limit: 99053,
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `code`                                                                                              | [operations.GetMyLinkedInProfileCode](../../models/operations/get-my-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `message`                                                                                           | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `docs`                                                                                              | *string*                                                                                            | :heavy_minus_sign:                                                                                  | N/A                                                                                                 |
| `retryAfter`                                                                                        | *number*                                                                                            | :heavy_check_mark:                                                                                  | Seconds to wait before retrying.                                                                    |
| `daily`                                                                                             | [operations.GetMyLinkedInProfileDaily](../../models/operations/get-my-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                  | Current and max daily usage (null if no daily cap).                                                 |
| `weekly`                                                                                            | [operations.GetMyLinkedInProfileWeekly](../../models/operations/get-my-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                  | Current and max weekly usage (null if no weekly cap).                                               |