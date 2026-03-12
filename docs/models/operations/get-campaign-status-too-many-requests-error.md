# GetCampaignStatusTooManyRequestsError

## Example Usage

```typescript
import { GetCampaignStatusTooManyRequestsError } from "bereach/models/operations";

let value: GetCampaignStatusTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 307248,
  daily: {
    current: 2027,
    limit: 922655,
  },
  weekly: {
    current: 873699,
    limit: 415605,
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `code`                                                                                      | [operations.GetCampaignStatusCode](../../models/operations/get-campaign-status-code.md)     | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `message`                                                                                   | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `docs`                                                                                      | *string*                                                                                    | :heavy_minus_sign:                                                                          | N/A                                                                                         |
| `retryAfter`                                                                                | *number*                                                                                    | :heavy_check_mark:                                                                          | Seconds to wait before retrying.                                                            |
| `daily`                                                                                     | [operations.GetCampaignStatusDaily](../../models/operations/get-campaign-status-daily.md)   | :heavy_check_mark:                                                                          | Current and max daily usage (null if no daily cap).                                         |
| `weekly`                                                                                    | [operations.GetCampaignStatusWeekly](../../models/operations/get-campaign-status-weekly.md) | :heavy_check_mark:                                                                          | Current and max weekly usage (null if no weekly cap).                                       |