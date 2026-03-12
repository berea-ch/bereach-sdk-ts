# FollowLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { FollowLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: FollowLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 522681,
  daily: {
    current: 553486,
    limit: 943914,
  },
  weekly: {
    current: 442721,
    limit: 851347,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `code`                                                                                               | [operations.FollowLinkedInProfileCode](../../models/operations/follow-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `message`                                                                                            | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `docs`                                                                                               | *string*                                                                                             | :heavy_minus_sign:                                                                                   | N/A                                                                                                  |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before retrying.                                                                     |
| `daily`                                                                                              | [operations.FollowLinkedInProfileDaily](../../models/operations/follow-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                   | Current and max daily usage (null if no daily cap).                                                  |
| `weekly`                                                                                             | [operations.FollowLinkedInProfileWeekly](../../models/operations/follow-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                   | Current and max weekly usage (null if no weekly cap).                                                |