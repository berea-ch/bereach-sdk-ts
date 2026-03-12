# GetMyLinkedInFollowersTooManyRequestsError

## Example Usage

```typescript
import { GetMyLinkedInFollowersTooManyRequestsError } from "bereach/models/operations";

let value: GetMyLinkedInFollowersTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 392785,
  daily: {
    current: 134590,
    limit: 842679,
  },
  weekly: {
    current: 807477,
    limit: 638418,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                  | [operations.GetMyLinkedInFollowersCode](../../models/operations/get-my-linked-in-followers-code.md)     | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `message`                                                                                               | *string*                                                                                                | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `docs`                                                                                                  | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `retryAfter`                                                                                            | *number*                                                                                                | :heavy_check_mark:                                                                                      | Seconds to wait before retrying.                                                                        |
| `daily`                                                                                                 | [operations.GetMyLinkedInFollowersDaily](../../models/operations/get-my-linked-in-followers-daily.md)   | :heavy_check_mark:                                                                                      | Current and max daily usage (null if no daily cap).                                                     |
| `weekly`                                                                                                | [operations.GetMyLinkedInFollowersWeekly](../../models/operations/get-my-linked-in-followers-weekly.md) | :heavy_check_mark:                                                                                      | Current and max weekly usage (null if no weekly cap).                                                   |