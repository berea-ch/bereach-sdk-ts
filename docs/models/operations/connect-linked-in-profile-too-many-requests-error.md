# ConnectLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { ConnectLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: ConnectLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 47220,
  daily: {
    current: 991676,
    limit: 476502,
  },
  weekly: {
    current: 622116,
    limit: 188106,
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `code`                                                                                                 | [operations.ConnectLinkedInProfileCode](../../models/operations/connect-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `message`                                                                                              | *string*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `docs`                                                                                                 | *string*                                                                                               | :heavy_minus_sign:                                                                                     | N/A                                                                                                    |
| `retryAfter`                                                                                           | *number*                                                                                               | :heavy_check_mark:                                                                                     | Seconds to wait before retrying.                                                                       |
| `daily`                                                                                                | [operations.ConnectLinkedInProfileDaily](../../models/operations/connect-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                     | Current and max daily usage (null if no daily cap).                                                    |
| `weekly`                                                                                               | [operations.ConnectLinkedInProfileWeekly](../../models/operations/connect-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                     | Current and max weekly usage (null if no weekly cap).                                                  |