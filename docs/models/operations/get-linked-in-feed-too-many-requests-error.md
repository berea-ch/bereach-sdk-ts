# GetLinkedInFeedTooManyRequestsError

## Example Usage

```typescript
import { GetLinkedInFeedTooManyRequestsError } from "bereach/models/operations";

let value: GetLinkedInFeedTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 870184,
  daily: {
    current: 879788,
    limit: 151980,
  },
  weekly: {
    current: 555511,
    limit: 360272,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `code`                                                                                   | [operations.GetLinkedInFeedCode](../../models/operations/get-linked-in-feed-code.md)     | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `message`                                                                                | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `docs`                                                                                   | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before retrying.                                                         |
| `daily`                                                                                  | [operations.GetLinkedInFeedDaily](../../models/operations/get-linked-in-feed-daily.md)   | :heavy_check_mark:                                                                       | Current and max daily usage (null if no daily cap).                                      |
| `weekly`                                                                                 | [operations.GetLinkedInFeedWeekly](../../models/operations/get-linked-in-feed-weekly.md) | :heavy_check_mark:                                                                       | Current and max weekly usage (null if no weekly cap).                                    |