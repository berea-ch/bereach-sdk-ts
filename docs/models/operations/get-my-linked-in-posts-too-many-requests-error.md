# GetMyLinkedInPostsTooManyRequestsError

## Example Usage

```typescript
import { GetMyLinkedInPostsTooManyRequestsError } from "bereach/models/operations";

let value: GetMyLinkedInPostsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 864939,
  daily: {
    current: 32494,
    limit: 944117,
  },
  weekly: {
    current: 451000,
    limit: 915920,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `code`                                                                                          | [operations.GetMyLinkedInPostsCode](../../models/operations/get-my-linked-in-posts-code.md)     | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `message`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `docs`                                                                                          | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `retryAfter`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | Seconds to wait before retrying.                                                                |
| `daily`                                                                                         | [operations.GetMyLinkedInPostsDaily](../../models/operations/get-my-linked-in-posts-daily.md)   | :heavy_check_mark:                                                                              | Current and max daily usage (null if no daily cap).                                             |
| `weekly`                                                                                        | [operations.GetMyLinkedInPostsWeekly](../../models/operations/get-my-linked-in-posts-weekly.md) | :heavy_check_mark:                                                                              | Current and max weekly usage (null if no weekly cap).                                           |