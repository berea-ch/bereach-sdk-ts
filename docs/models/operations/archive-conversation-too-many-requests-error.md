# ArchiveConversationTooManyRequestsError

## Example Usage

```typescript
import { ArchiveConversationTooManyRequestsError } from "bereach/models/operations";

let value: ArchiveConversationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 739238,
  daily: {
    current: 269414,
    limit: 428312,
  },
  weekly: {
    current: 765988,
    limit: 509392,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `code`                                                                                         | [operations.ArchiveConversationCode](../../models/operations/archive-conversation-code.md)     | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `message`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `docs`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before retrying.                                                               |
| `daily`                                                                                        | [operations.ArchiveConversationDaily](../../models/operations/archive-conversation-daily.md)   | :heavy_check_mark:                                                                             | Current and max daily usage (null if no daily cap).                                            |
| `weekly`                                                                                       | [operations.ArchiveConversationWeekly](../../models/operations/archive-conversation-weekly.md) | :heavy_check_mark:                                                                             | Current and max weekly usage (null if no weekly cap).                                          |