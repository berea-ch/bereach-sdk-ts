# SearchSalesNavPeopleTooManyRequestsError

## Example Usage

```typescript
import { SearchSalesNavPeopleTooManyRequestsError } from "bereach/models/operations";

let value: SearchSalesNavPeopleTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 123466,
  daily: {
    current: 751377,
    limit: 47462,
  },
  weekly: {
    current: 687973,
    limit: 238152,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.SearchSalesNavPeopleCode](../../models/operations/search-sales-nav-people-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.SearchSalesNavPeopleDaily](../../models/operations/search-sales-nav-people-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.SearchSalesNavPeopleWeekly](../../models/operations/search-sales-nav-people-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |