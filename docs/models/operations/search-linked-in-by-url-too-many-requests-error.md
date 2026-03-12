# SearchLinkedInByUrlTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInByUrlTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInByUrlTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 808997,
  daily: {
    current: 379061,
    limit: 66739,
  },
  weekly: {
    current: 847528,
    limit: 885129,
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `code`                                                                                            | [operations.SearchLinkedInByUrlCode](../../models/operations/search-linked-in-by-url-code.md)     | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `message`                                                                                         | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `docs`                                                                                            | *string*                                                                                          | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `retryAfter`                                                                                      | *number*                                                                                          | :heavy_check_mark:                                                                                | Seconds to wait before retrying.                                                                  |
| `daily`                                                                                           | [operations.SearchLinkedInByUrlDaily](../../models/operations/search-linked-in-by-url-daily.md)   | :heavy_check_mark:                                                                                | Current and max daily usage (null if no daily cap).                                               |
| `weekly`                                                                                          | [operations.SearchLinkedInByUrlWeekly](../../models/operations/search-linked-in-by-url-weekly.md) | :heavy_check_mark:                                                                                | Current and max weekly usage (null if no weekly cap).                                             |