# UnreactToMessageTooManyRequestsError

## Example Usage

```typescript
import { UnreactToMessageTooManyRequestsError } from "bereach/models/operations";

let value: UnreactToMessageTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 313788,
  daily: {
    current: 713276,
    limit: 2508,
  },
  weekly: null,
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `code`                                                                                    | [operations.UnreactToMessageCode](../../models/operations/unreact-to-message-code.md)     | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `message`                                                                                 | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `docs`                                                                                    | *string*                                                                                  | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `retryAfter`                                                                              | *number*                                                                                  | :heavy_check_mark:                                                                        | Seconds to wait before retrying.                                                          |
| `daily`                                                                                   | [operations.UnreactToMessageDaily](../../models/operations/unreact-to-message-daily.md)   | :heavy_check_mark:                                                                        | Current and max daily usage (null if no daily cap).                                       |
| `weekly`                                                                                  | [operations.UnreactToMessageWeekly](../../models/operations/unreact-to-message-weekly.md) | :heavy_check_mark:                                                                        | Current and max weekly usage (null if no weekly cap).                                     |