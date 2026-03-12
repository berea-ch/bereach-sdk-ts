# GetCompanyPageAnalyticsTooManyRequestsError

## Example Usage

```typescript
import { GetCompanyPageAnalyticsTooManyRequestsError } from "bereach/models/operations";

let value: GetCompanyPageAnalyticsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 737012,
  daily: {
    current: 795003,
    limit: 191576,
  },
  weekly: {
    current: 738393,
    limit: 673280,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.GetCompanyPageAnalyticsCode](../../models/operations/get-company-page-analytics-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.GetCompanyPageAnalyticsDaily](../../models/operations/get-company-page-analytics-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.GetCompanyPageAnalyticsWeekly](../../models/operations/get-company-page-analytics-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |