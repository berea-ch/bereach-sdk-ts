# GetLinkedInFollowerAnalyticsTooManyRequestsError

## Example Usage

```typescript
import { GetLinkedInFollowerAnalyticsTooManyRequestsError } from "bereach/models/operations";

let value: GetLinkedInFollowerAnalyticsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 792749,
  daily: {
    current: 287022,
    limit: 133815,
  },
  weekly: {
    current: 297945,
    limit: 746612,
  },
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                              | [operations.GetLinkedInFollowerAnalyticsCode](../../models/operations/get-linked-in-follower-analytics-code.md)     | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `message`                                                                                                           | *string*                                                                                                            | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `docs`                                                                                                              | *string*                                                                                                            | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before retrying.                                                                                    |
| `daily`                                                                                                             | [operations.GetLinkedInFollowerAnalyticsDaily](../../models/operations/get-linked-in-follower-analytics-daily.md)   | :heavy_check_mark:                                                                                                  | Current and max daily usage (null if no daily cap).                                                                 |
| `weekly`                                                                                                            | [operations.GetLinkedInFollowerAnalyticsWeekly](../../models/operations/get-linked-in-follower-analytics-weekly.md) | :heavy_check_mark:                                                                                                  | Current and max weekly usage (null if no weekly cap).                                                               |