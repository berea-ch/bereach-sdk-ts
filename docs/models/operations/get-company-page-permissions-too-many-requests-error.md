# GetCompanyPagePermissionsTooManyRequestsError

## Example Usage

```typescript
import { GetCompanyPagePermissionsTooManyRequestsError } from "bereach/models/operations";

let value: GetCompanyPagePermissionsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 274954,
  daily: {
    current: 355711,
    limit: 736672,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `code`                                                                                                       | [operations.GetCompanyPagePermissionsCode](../../models/operations/get-company-page-permissions-code.md)     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `message`                                                                                                    | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `docs`                                                                                                       | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | N/A                                                                                                          |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before retrying.                                                                             |
| `daily`                                                                                                      | [operations.GetCompanyPagePermissionsDaily](../../models/operations/get-company-page-permissions-daily.md)   | :heavy_check_mark:                                                                                           | Current and max daily usage (null if no daily cap).                                                          |
| `weekly`                                                                                                     | [operations.GetCompanyPagePermissionsWeekly](../../models/operations/get-company-page-permissions-weekly.md) | :heavy_check_mark:                                                                                           | Current and max weekly usage (null if no weekly cap).                                                        |