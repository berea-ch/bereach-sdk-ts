# GetLinkedInPostAnalyticsTooManyRequestsError

## Example Usage

```typescript
import { GetLinkedInPostAnalyticsTooManyRequestsError } from "bereach/models/operations";

let value: GetLinkedInPostAnalyticsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 441991,
  daily: {
    current: 950471,
    limit: 538949,
  },
  weekly: {
    current: 301191,
    limit: 905729,
  },
};
```

## Fields

| Field                                                                                                       | Type                                                                                                        | Required                                                                                                    | Description                                                                                                 |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                      | [operations.GetLinkedInPostAnalyticsCode](../../models/operations/get-linked-in-post-analytics-code.md)     | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `message`                                                                                                   | *string*                                                                                                    | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `docs`                                                                                                      | *string*                                                                                                    | :heavy_minus_sign:                                                                                          | N/A                                                                                                         |
| `retryAfter`                                                                                                | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Seconds to wait before retrying.                                                                            |
| `daily`                                                                                                     | [operations.GetLinkedInPostAnalyticsDaily](../../models/operations/get-linked-in-post-analytics-daily.md)   | :heavy_check_mark:                                                                                          | Current and max daily usage (null if no daily cap).                                                         |
| `weekly`                                                                                                    | [operations.GetLinkedInPostAnalyticsWeekly](../../models/operations/get-linked-in-post-analytics-weekly.md) | :heavy_check_mark:                                                                                          | Current and max weekly usage (null if no weekly cap).                                                       |