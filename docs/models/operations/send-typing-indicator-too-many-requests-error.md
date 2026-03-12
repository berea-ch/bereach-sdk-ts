# SendTypingIndicatorTooManyRequestsError

## Example Usage

```typescript
import { SendTypingIndicatorTooManyRequestsError } from "bereach/models/operations";

let value: SendTypingIndicatorTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 555922,
  daily: {
    current: 78667,
    limit: 385747,
  },
  weekly: {
    current: 608879,
    limit: 165812,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `code`                                                                                          | [operations.SendTypingIndicatorCode](../../models/operations/send-typing-indicator-code.md)     | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `message`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `docs`                                                                                          | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `retryAfter`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | Seconds to wait before retrying.                                                                |
| `daily`                                                                                         | [operations.SendTypingIndicatorDaily](../../models/operations/send-typing-indicator-daily.md)   | :heavy_check_mark:                                                                              | Current and max daily usage (null if no daily cap).                                             |
| `weekly`                                                                                        | [operations.SendTypingIndicatorWeekly](../../models/operations/send-typing-indicator-weekly.md) | :heavy_check_mark:                                                                              | Current and max weekly usage (null if no weekly cap).                                           |