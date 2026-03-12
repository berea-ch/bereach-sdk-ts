# GetCompanyPagePostsTooManyRequestsError

## Example Usage

```typescript
import { GetCompanyPagePostsTooManyRequestsError } from "bereach/models/operations";

let value: GetCompanyPagePostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 889757,
  daily: {
    current: 430877,
    limit: 486854,
  },
  weekly: {
    current: 585599,
    limit: 857186,
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `code`                                                                                           | [operations.GetCompanyPagePostsCode](../../models/operations/get-company-page-posts-code.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `message`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `docs`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before retrying.                                                                 |
| `daily`                                                                                          | [operations.GetCompanyPagePostsDaily](../../models/operations/get-company-page-posts-daily.md)   | :heavy_check_mark:                                                                               | Current and max daily usage (null if no daily cap).                                              |
| `weekly`                                                                                         | [operations.GetCompanyPagePostsWeekly](../../models/operations/get-company-page-posts-weekly.md) | :heavy_check_mark:                                                                               | Current and max weekly usage (null if no weekly cap).                                            |