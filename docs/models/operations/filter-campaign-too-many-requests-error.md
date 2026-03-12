# FilterCampaignTooManyRequestsError

## Example Usage

```typescript
import { FilterCampaignTooManyRequestsError } from "bereach/models/operations";

let value: FilterCampaignTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 436895,
  daily: {
    current: 229932,
    limit: 731901,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `code`                                                                               | [operations.FilterCampaignCode](../../models/operations/filter-campaign-code.md)     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `message`                                                                            | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `docs`                                                                               | *string*                                                                             | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before retrying.                                                     |
| `daily`                                                                              | [operations.FilterCampaignDaily](../../models/operations/filter-campaign-daily.md)   | :heavy_check_mark:                                                                   | Current and max daily usage (null if no daily cap).                                  |
| `weekly`                                                                             | [operations.FilterCampaignWeekly](../../models/operations/filter-campaign-weekly.md) | :heavy_check_mark:                                                                   | Current and max weekly usage (null if no weekly cap).                                |