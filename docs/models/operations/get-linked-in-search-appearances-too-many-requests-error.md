# GetLinkedInSearchAppearancesTooManyRequestsError

## Example Usage

```typescript
import { GetLinkedInSearchAppearancesTooManyRequestsError } from "bereach/models/operations";

let value: GetLinkedInSearchAppearancesTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 763433,
  daily: {
    current: 947314,
    limit: 45893,
  },
  weekly: {
    current: 838722,
    limit: 747277,
  },
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                              | [operations.GetLinkedInSearchAppearancesCode](../../models/operations/get-linked-in-search-appearances-code.md)     | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `message`                                                                                                           | *string*                                                                                                            | :heavy_check_mark:                                                                                                  | N/A                                                                                                                 |
| `docs`                                                                                                              | *string*                                                                                                            | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |
| `retryAfter`                                                                                                        | *number*                                                                                                            | :heavy_check_mark:                                                                                                  | Seconds to wait before retrying.                                                                                    |
| `daily`                                                                                                             | [operations.GetLinkedInSearchAppearancesDaily](../../models/operations/get-linked-in-search-appearances-daily.md)   | :heavy_check_mark:                                                                                                  | Current and max daily usage (null if no daily cap).                                                                 |
| `weekly`                                                                                                            | [operations.GetLinkedInSearchAppearancesWeekly](../../models/operations/get-linked-in-search-appearances-weekly.md) | :heavy_check_mark:                                                                                                  | Current and max weekly usage (null if no weekly cap).                                                               |