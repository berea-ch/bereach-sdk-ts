# SearchSalesNavCompaniesTooManyRequestsError

## Example Usage

```typescript
import { SearchSalesNavCompaniesTooManyRequestsError } from "bereach/models/operations";

let value: SearchSalesNavCompaniesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 180806,
  daily: {
    current: 974742,
    limit: 3135,
  },
  weekly: {
    current: 809942,
    limit: 377965,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.SearchSalesNavCompaniesCode](../../models/operations/search-sales-nav-companies-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.SearchSalesNavCompaniesDaily](../../models/operations/search-sales-nav-companies-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.SearchSalesNavCompaniesWeekly](../../models/operations/search-sales-nav-companies-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |