# GetCampaignStatsTooManyRequestsError

## Example Usage

```typescript
import { GetCampaignStatsTooManyRequestsError } from "bereach/models/operations";

let value: GetCampaignStatsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 915279,
  daily: {
    current: 118877,
    limit: 320245,
  },
  weekly: {
    current: 96582,
    limit: 435503,
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `code`                                                                                    | [operations.GetCampaignStatsCode](../../models/operations/get-campaign-stats-code.md)     | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `message`                                                                                 | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `docs`                                                                                    | *string*                                                                                  | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `retryAfter`                                                                              | *number*                                                                                  | :heavy_check_mark:                                                                        | Seconds to wait before retrying.                                                          |
| `daily`                                                                                   | [operations.GetCampaignStatsDaily](../../models/operations/get-campaign-stats-daily.md)   | :heavy_check_mark:                                                                        | Current and max daily usage (null if no daily cap).                                       |
| `weekly`                                                                                  | [operations.GetCampaignStatsWeekly](../../models/operations/get-campaign-stats-weekly.md) | :heavy_check_mark:                                                                        | Current and max weekly usage (null if no weekly cap).                                     |