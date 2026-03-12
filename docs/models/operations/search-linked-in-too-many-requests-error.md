# SearchLinkedInTooManyRequestsError

## Example Usage

```typescript
import { SearchLinkedInTooManyRequestsError } from "bereach/models/operations";

let value: SearchLinkedInTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 612394,
  daily: {
    current: 235212,
    limit: 978947,
  },
  weekly: {
    current: 381810,
    limit: 141059,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `code`                                                                                | [operations.SearchLinkedInCode](../../models/operations/search-linked-in-code.md)     | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `message`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `docs`                                                                                | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `retryAfter`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | Seconds to wait before retrying.                                                      |
| `daily`                                                                               | [operations.SearchLinkedInDaily](../../models/operations/search-linked-in-daily.md)   | :heavy_check_mark:                                                                    | Current and max daily usage (null if no daily cap).                                   |
| `weekly`                                                                              | [operations.SearchLinkedInWeekly](../../models/operations/search-linked-in-weekly.md) | :heavy_check_mark:                                                                    | Current and max weekly usage (null if no weekly cap).                                 |