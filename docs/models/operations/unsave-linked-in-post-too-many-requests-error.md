# UnsaveLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { UnsaveLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: UnsaveLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 761053,
  daily: {
    current: 425680,
    limit: 370663,
  },
  weekly: {
    current: 496490,
    limit: 618445,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `code`                                                                                         | [operations.UnsaveLinkedInPostCode](../../models/operations/unsave-linked-in-post-code.md)     | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `message`                                                                                      | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `docs`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `retryAfter`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | Seconds to wait before retrying.                                                               |
| `daily`                                                                                        | [operations.UnsaveLinkedInPostDaily](../../models/operations/unsave-linked-in-post-daily.md)   | :heavy_check_mark:                                                                             | Current and max daily usage (null if no daily cap).                                            |
| `weekly`                                                                                       | [operations.UnsaveLinkedInPostWeekly](../../models/operations/unsave-linked-in-post-weekly.md) | :heavy_check_mark:                                                                             | Current and max weekly usage (null if no weekly cap).                                          |