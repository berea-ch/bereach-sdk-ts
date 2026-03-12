# ReactToMessageTooManyRequestsError

## Example Usage

```typescript
import { ReactToMessageTooManyRequestsError } from "bereach/models/operations";

let value: ReactToMessageTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 282811,
  daily: {
    current: 884139,
    limit: 585767,
  },
  weekly: {
    current: 886821,
    limit: 558209,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `code`                                                                                | [operations.ReactToMessageCode](../../models/operations/react-to-message-code.md)     | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `message`                                                                             | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `docs`                                                                                | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `retryAfter`                                                                          | *number*                                                                              | :heavy_check_mark:                                                                    | Seconds to wait before retrying.                                                      |
| `daily`                                                                               | [operations.ReactToMessageDaily](../../models/operations/react-to-message-daily.md)   | :heavy_check_mark:                                                                    | Current and max daily usage (null if no daily cap).                                   |
| `weekly`                                                                              | [operations.ReactToMessageWeekly](../../models/operations/react-to-message-weekly.md) | :heavy_check_mark:                                                                    | Current and max weekly usage (null if no weekly cap).                                 |