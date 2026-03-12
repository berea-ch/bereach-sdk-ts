# RepostLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { RepostLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: RepostLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 391136,
  daily: {
    current: 687139,
    limit: 560704,
  },
  weekly: {
    current: 693186,
    limit: 385737,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `code`                                                                                         | [operations.RepostLinkedInPostCode](../../models/operations/repost-linked-in-post-code.md)     | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `message`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `docs`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before retrying.                                                               |
| `daily`                                                                                        | [operations.RepostLinkedInPostDaily](../../models/operations/repost-linked-in-post-daily.md)   | :heavy_check_mark:                                                                             | Current and max daily usage (null if no daily cap).                                            |
| `weekly`                                                                                       | [operations.RepostLinkedInPostWeekly](../../models/operations/repost-linked-in-post-weekly.md) | :heavy_check_mark:                                                                             | Current and max weekly usage (null if no weekly cap).                                          |