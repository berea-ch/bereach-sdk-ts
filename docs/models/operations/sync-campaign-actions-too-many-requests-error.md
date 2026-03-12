# SyncCampaignActionsTooManyRequestsError

## Example Usage

```typescript
import { SyncCampaignActionsTooManyRequestsError } from "bereach/models/operations";

let value: SyncCampaignActionsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 404676,
  daily: {
    current: 505069,
    limit: 458534,
  },
  weekly: {
    current: 247120,
    limit: 684502,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `code`                                                                                          | [operations.SyncCampaignActionsCode](../../models/operations/sync-campaign-actions-code.md)     | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `message`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `docs`                                                                                          | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `retryAfter`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | Seconds to wait before retrying.                                                                |
| `daily`                                                                                         | [operations.SyncCampaignActionsDaily](../../models/operations/sync-campaign-actions-daily.md)   | :heavy_check_mark:                                                                              | Current and max daily usage (null if no daily cap).                                             |
| `weekly`                                                                                        | [operations.SyncCampaignActionsWeekly](../../models/operations/sync-campaign-actions-weekly.md) | :heavy_check_mark:                                                                              | Current and max weekly usage (null if no weekly cap).                                           |