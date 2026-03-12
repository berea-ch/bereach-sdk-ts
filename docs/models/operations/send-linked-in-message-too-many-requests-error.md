# SendLinkedInMessageTooManyRequestsError

## Example Usage

```typescript
import { SendLinkedInMessageTooManyRequestsError } from "bereach/models/operations";

let value: SendLinkedInMessageTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 353164,
  daily: {
    current: 791588,
    limit: 243541,
  },
  weekly: {
    current: 824667,
    limit: 28007,
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `code`                                                                                           | [operations.SendLinkedInMessageCode](../../models/operations/send-linked-in-message-code.md)     | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `message`                                                                                        | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `docs`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before retrying.                                                                 |
| `daily`                                                                                          | [operations.SendLinkedInMessageDaily](../../models/operations/send-linked-in-message-daily.md)   | :heavy_check_mark:                                                                               | Current and max daily usage (null if no daily cap).                                              |
| `weekly`                                                                                         | [operations.SendLinkedInMessageWeekly](../../models/operations/send-linked-in-message-weekly.md) | :heavy_check_mark:                                                                               | Current and max weekly usage (null if no weekly cap).                                            |