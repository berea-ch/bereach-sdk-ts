# SearchLinkedInJobsTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInJobsTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInJobsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 496124,
  daily: {
    current: 396712,
    limit: 498903,
  },
  weekly: {
    current: 235245,
    limit: 536345,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `code`                                                                                         | [operations.SearchLinkedInJobsCode](../../models/operations/search-linked-in-jobs-code.md)     | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `message`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `docs`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before retrying.                                                               |
| `daily`                                                                                        | [operations.SearchLinkedInJobsDaily](../../models/operations/search-linked-in-jobs-daily.md)   | :heavy_check_mark:                                                                             | Current and max daily usage (null if no daily cap).                                            |
| `weekly`                                                                                       | [operations.SearchLinkedInJobsWeekly](../../models/operations/search-linked-in-jobs-weekly.md) | :heavy_check_mark:                                                                             | Current and max weekly usage (null if no weekly cap).                                          |