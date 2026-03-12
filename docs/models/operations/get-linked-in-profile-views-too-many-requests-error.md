# GetLinkedInProfileViewsTooManyRequestsError

## Example Usage

```typescript
import { GetLinkedInProfileViewsTooManyRequestsError } from "bereach/models/operations";

let value: GetLinkedInProfileViewsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 438073,
  daily: {
    current: 541995,
    limit: 462896,
  },
  weekly: {
    current: 394689,
    limit: 574788,
  },
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                    | [operations.GetLinkedInProfileViewsCode](../../models/operations/get-linked-in-profile-views-code.md)     | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `message`                                                                                                 | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `docs`                                                                                                    | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `retryAfter`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Seconds to wait before retrying.                                                                          |
| `daily`                                                                                                   | [operations.GetLinkedInProfileViewsDaily](../../models/operations/get-linked-in-profile-views-daily.md)   | :heavy_check_mark:                                                                                        | Current and max daily usage (null if no daily cap).                                                       |
| `weekly`                                                                                                  | [operations.GetLinkedInProfileViewsWeekly](../../models/operations/get-linked-in-profile-views-weekly.md) | :heavy_check_mark:                                                                                        | Current and max weekly usage (null if no weekly cap).                                                     |