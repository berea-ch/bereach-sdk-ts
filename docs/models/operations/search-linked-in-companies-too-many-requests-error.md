# SearchLinkedInCompaniesTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInCompaniesTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInCompaniesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 821626,
  daily: {
    current: 206782,
    limit: 696264,
  },
  weekly: {
    current: 575434,
    limit: 41506,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.SearchLinkedInCompaniesCode](../../models/operations/search-linked-in-companies-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.SearchLinkedInCompaniesDaily](../../models/operations/search-linked-in-companies-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.SearchLinkedInCompaniesWeekly](../../models/operations/search-linked-in-companies-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |