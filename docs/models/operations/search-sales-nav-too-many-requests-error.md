# SearchSalesNavTooManyRequestsError

## Example Usage

```typescript
import { SearchSalesNavTooManyRequestsError } from "bereach/models/operations";

let value: SearchSalesNavTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 354410,
  daily: {
    current: 978474,
    limit: 821784,
  },
  weekly: {
    current: 221896,
    limit: 679818,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `code`                                                                                | [operations.SearchSalesNavCode](../../models/operations/search-sales-nav-code.md)     | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `message`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `docs`                                                                                | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `retryAfter`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | Seconds to wait before retrying.                                                      |
| `daily`                                                                               | [operations.SearchSalesNavDaily](../../models/operations/search-sales-nav-daily.md)   | :heavy_check_mark:                                                                    | Current and max daily usage (null if no daily cap).                                   |
| `weekly`                                                                              | [operations.SearchSalesNavWeekly](../../models/operations/search-sales-nav-weekly.md) | :heavy_check_mark:                                                                    | Current and max weekly usage (null if no weekly cap).                                 |