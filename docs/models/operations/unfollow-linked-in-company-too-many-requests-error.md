# UnfollowLinkedInCompanyTooManyRequestsError

## Example Usage

```typescript
import { UnfollowLinkedInCompanyTooManyRequestsError } from "bereach/models/operations";

let value: UnfollowLinkedInCompanyTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 24391,
  daily: {
    current: 253941,
    limit: 897820,
  },
  weekly: {
    current: 640572,
    limit: 674498,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.UnfollowLinkedInCompanyCode](../../models/operations/unfollow-linked-in-company-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.UnfollowLinkedInCompanyDaily](../../models/operations/unfollow-linked-in-company-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.UnfollowLinkedInCompanyWeekly](../../models/operations/unfollow-linked-in-company-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |