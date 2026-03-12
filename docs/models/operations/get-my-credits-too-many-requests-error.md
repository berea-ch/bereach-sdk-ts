# GetMyCreditsTooManyRequestsError

## Example Usage

```typescript
import { GetMyCreditsTooManyRequestsError } from "bereach/models/operations";

let value: GetMyCreditsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 13722,
  daily: {
    current: 493922,
    limit: 22055,
  },
  weekly: {
    current: 572202,
    limit: 717892,
  },
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `code`                                                                            | [operations.GetMyCreditsCode](../../models/operations/get-my-credits-code.md)     | :heavy_check_mark:                                                                | N/A                                                                               |
| `message`                                                                         | *string*                                                                          | :heavy_check_mark:                                                                | N/A                                                                               |
| `docs`                                                                            | *string*                                                                          | :heavy_minus_sign:                                                                | N/A                                                                               |
| `retryAfter`                                                                      | *number*                                                                          | :heavy_check_mark:                                                                | Seconds to wait before retrying.                                                  |
| `daily`                                                                           | [operations.GetMyCreditsDaily](../../models/operations/get-my-credits-daily.md)   | :heavy_check_mark:                                                                | Current and max daily usage (null if no daily cap).                               |
| `weekly`                                                                          | [operations.GetMyCreditsWeekly](../../models/operations/get-my-credits-weekly.md) | :heavy_check_mark:                                                                | Current and max weekly usage (null if no weekly cap).                             |