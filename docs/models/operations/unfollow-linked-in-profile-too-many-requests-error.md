# UnfollowLinkedInProfileTooManyRequestsError

## Example Usage

```typescript
import { UnfollowLinkedInProfileTooManyRequestsError } from "bereach/models/operations";

let value: UnfollowLinkedInProfileTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 328577,
  daily: {
    current: 574719,
    limit: 425426,
  },
  weekly: {
    current: 541669,
    limit: 965475,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.UnfollowLinkedInProfileCode](../../models/operations/unfollow-linked-in-profile-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.UnfollowLinkedInProfileDaily](../../models/operations/unfollow-linked-in-profile-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.UnfollowLinkedInProfileWeekly](../../models/operations/unfollow-linked-in-profile-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |