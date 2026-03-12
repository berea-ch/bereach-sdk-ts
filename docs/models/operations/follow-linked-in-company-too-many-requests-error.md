# FollowLinkedInCompanyTooManyRequestsError

## Example Usage

```typescript
import { FollowLinkedInCompanyTooManyRequestsError } from "bereach/models/operations";

let value: FollowLinkedInCompanyTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 401328,
  daily: null,
  weekly: {
    current: 101371,
    limit: 237486,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `code`                                                                                               | [operations.FollowLinkedInCompanyCode](../../models/operations/follow-linked-in-company-code.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `message`                                                                                            | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `docs`                                                                                               | *string*                                                                                             | :heavy_minus_sign:                                                                                   | N/A                                                                                                  |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before retrying.                                                                     |
| `daily`                                                                                              | [operations.FollowLinkedInCompanyDaily](../../models/operations/follow-linked-in-company-daily.md)   | :heavy_check_mark:                                                                                   | Current and max daily usage (null if no daily cap).                                                  |
| `weekly`                                                                                             | [operations.FollowLinkedInCompanyWeekly](../../models/operations/follow-linked-in-company-weekly.md) | :heavy_check_mark:                                                                                   | Current and max weekly usage (null if no weekly cap).                                                |