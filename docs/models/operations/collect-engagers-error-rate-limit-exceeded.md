# CollectEngagersErrorRateLimitExceeded

## Example Usage

```typescript
import { CollectEngagersErrorRateLimitExceeded } from "bereach/models/operations";

let value: CollectEngagersErrorRateLimitExceeded = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 525827,
  daily: {
    current: 104757,
    limit: 311202,
  },
  weekly: {
    current: 28490,
    limit: 522524,
  },
};
```

## Fields

| Field                                                                                                                              | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                                             | [operations.CollectEngagersCode](../../models/operations/collect-engagers-code.md)                                                 | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `message`                                                                                                                          | *string*                                                                                                                           | :heavy_check_mark:                                                                                                                 | N/A                                                                                                                                |
| `docs`                                                                                                                             | *string*                                                                                                                           | :heavy_minus_sign:                                                                                                                 | N/A                                                                                                                                |
| `retryAfter`                                                                                                                       | *number*                                                                                                                           | :heavy_check_mark:                                                                                                                 | Seconds to wait before retrying.                                                                                                   |
| `daily`                                                                                                                            | [operations.CollectEngagersDaily](../../models/operations/collect-engagers-daily.md)                                               | :heavy_check_mark:                                                                                                                 | Current and max daily usage (null if no daily cap).                                                                                |
| `weekly`                                                                                                                           | [operations.CollectEngagersWeekly](../../models/operations/collect-engagers-weekly.md)                                             | :heavy_check_mark:                                                                                                                 | Current and max weekly usage (null if no weekly cap).                                                                              |
| `quotaKind`                                                                                                                        | [operations.CollectEngagersQuotaKindRateLimitExceeded](../../models/operations/collect-engagers-quota-kind-rate-limit-exceeded.md) | :heavy_minus_sign:                                                                                                                 | Structured classification so clients can route to the right banner without keyword matching.                                       |