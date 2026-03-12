# GetUnreadCountTooManyRequestsError

## Example Usage

```typescript
import { GetUnreadCountTooManyRequestsError } from "bereach/models/operations";

let value: GetUnreadCountTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 995404,
  daily: {
    current: 132902,
    limit: 576626,
  },
  weekly: {
    current: 939293,
    limit: 545685,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `code`                                                                                | [operations.GetUnreadCountCode](../../models/operations/get-unread-count-code.md)     | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `message`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `docs`                                                                                | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `retryAfter`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | Seconds to wait before retrying.                                                      |
| `daily`                                                                               | [operations.GetUnreadCountDaily](../../models/operations/get-unread-count-daily.md)   | :heavy_check_mark:                                                                    | Current and max daily usage (null if no daily cap).                                   |
| `weekly`                                                                              | [operations.GetUnreadCountWeekly](../../models/operations/get-unread-count-weekly.md) | :heavy_check_mark:                                                                    | Current and max weekly usage (null if no weekly cap).                                 |