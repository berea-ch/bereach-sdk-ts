# CollectSavedLinkedInPostsTooManyRequestsError

## Example Usage

```typescript
import { CollectSavedLinkedInPostsTooManyRequestsError } from "bereach/models/operations";

let value: CollectSavedLinkedInPostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 484859,
  daily: {
    current: 335635,
    limit: 220871,
  },
  weekly: {
    current: 233044,
    limit: 67368,
  },
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                        | [operations.CollectSavedLinkedInPostsCode](../../models/operations/collect-saved-linked-in-posts-code.md)     | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `message`                                                                                                     | *string*                                                                                                      | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `docs`                                                                                                        | *string*                                                                                                      | :heavy_minus_sign:                                                                                            | N/A                                                                                                           |
| `retryAfter`                                                                                                  | *number*                                                                                                      | :heavy_check_mark:                                                                                            | Seconds to wait before retrying.                                                                              |
| `daily`                                                                                                       | [operations.CollectSavedLinkedInPostsDaily](../../models/operations/collect-saved-linked-in-posts-daily.md)   | :heavy_check_mark:                                                                                            | Current and max daily usage (null if no daily cap).                                                           |
| `weekly`                                                                                                      | [operations.CollectSavedLinkedInPostsWeekly](../../models/operations/collect-saved-linked-in-posts-weekly.md) | :heavy_check_mark:                                                                                            | Current and max weekly usage (null if no weekly cap).                                                         |