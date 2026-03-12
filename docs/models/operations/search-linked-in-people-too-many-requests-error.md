# SearchLinkedInPeopleTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInPeopleTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInPeopleTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 335632,
  daily: {
    current: 230225,
    limit: 188003,
  },
  weekly: {
    current: 845319,
    limit: 139103,
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `code`                                                                                             | [operations.SearchLinkedInPeopleCode](../../models/operations/search-linked-in-people-code.md)     | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `message`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `docs`                                                                                             | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `retryAfter`                                                                                       | *number*                                                                                           | :heavy_check_mark:                                                                                 | Seconds to wait before retrying.                                                                   |
| `daily`                                                                                            | [operations.SearchLinkedInPeopleDaily](../../models/operations/search-linked-in-people-daily.md)   | :heavy_check_mark:                                                                                 | Current and max daily usage (null if no daily cap).                                                |
| `weekly`                                                                                           | [operations.SearchLinkedInPeopleWeekly](../../models/operations/search-linked-in-people-weekly.md) | :heavy_check_mark:                                                                                 | Current and max weekly usage (null if no weekly cap).                                              |