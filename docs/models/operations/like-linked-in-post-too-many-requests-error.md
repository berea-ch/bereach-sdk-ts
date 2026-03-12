# LikeLinkedInPostTooManyRequestsError

## Example Usage

```typescript
import { LikeLinkedInPostTooManyRequestsError } from "bereach/models/operations";

let value: LikeLinkedInPostTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 328166,
  daily: null,
  weekly: null,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `code`                                                                                     | [operations.LikeLinkedInPostCode](../../models/operations/like-linked-in-post-code.md)     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `message`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `docs`                                                                                     | *string*                                                                                   | :heavy_minus_sign:                                                                         | N/A                                                                                        |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before retrying.                                                           |
| `daily`                                                                                    | [operations.LikeLinkedInPostDaily](../../models/operations/like-linked-in-post-daily.md)   | :heavy_check_mark:                                                                         | Current and max daily usage (null if no daily cap).                                        |
| `weekly`                                                                                   | [operations.LikeLinkedInPostWeekly](../../models/operations/like-linked-in-post-weekly.md) | :heavy_check_mark:                                                                         | Current and max weekly usage (null if no weekly cap).                                      |