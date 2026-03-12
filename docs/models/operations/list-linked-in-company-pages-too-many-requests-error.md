# ListLinkedInCompanyPagesTooManyRequestsError

## Example Usage

```typescript
import { ListLinkedInCompanyPagesTooManyRequestsError } from "bereach/models/operations";

let value: ListLinkedInCompanyPagesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 317363,
  daily: {
    current: 273842,
    limit: 349144,
  },
  weekly: {
    current: 498646,
    limit: 768905,
  },
};
```

## Fields

| Field                                                                                                       | Type                                                                                                        | Required                                                                                                    | Description                                                                                                 |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                      | [operations.ListLinkedInCompanyPagesCode](../../models/operations/list-linked-in-company-pages-code.md)     | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `message`                                                                                                   | *string*                                                                                                    | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `docs`                                                                                                      | *string*                                                                                                    | :heavy_minus_sign:                                                                                          | N/A                                                                                                         |
| `retryAfter`                                                                                                | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Seconds to wait before retrying.                                                                            |
| `daily`                                                                                                     | [operations.ListLinkedInCompanyPagesDaily](../../models/operations/list-linked-in-company-pages-daily.md)   | :heavy_check_mark:                                                                                          | Current and max daily usage (null if no daily cap).                                                         |
| `weekly`                                                                                                    | [operations.ListLinkedInCompanyPagesWeekly](../../models/operations/list-linked-in-company-pages-weekly.md) | :heavy_check_mark:                                                                                          | Current and max weekly usage (null if no weekly cap).                                                       |