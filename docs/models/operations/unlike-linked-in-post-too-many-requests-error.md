# UnlikeLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { UnlikeLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: UnlikeLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 526119,
  daily: {
    current: 187952,
    limit: 4907,
  },
  weekly: {
    current: 331969,
    limit: 184469,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `code`                                                                                         | [operations.UnlikeLinkedInPostCode](../../models/operations/unlike-linked-in-post-code.md)     | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `message`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `docs`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before retrying.                                                               |
| `daily`                                                                                        | [operations.UnlikeLinkedInPostDaily](../../models/operations/unlike-linked-in-post-daily.md)   | :heavy_check_mark:                                                                             | Current and max daily usage (null if no daily cap).                                            |
| `weekly`                                                                                       | [operations.UnlikeLinkedInPostWeekly](../../models/operations/unlike-linked-in-post-weekly.md) | :heavy_check_mark:                                                                             | Current and max weekly usage (null if no weekly cap).                                          |