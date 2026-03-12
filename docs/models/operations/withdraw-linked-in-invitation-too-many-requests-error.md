# WithdrawLinkedInInvitationTooManyRequestsError

## Example Usage

```typescript
import { WithdrawLinkedInInvitationTooManyRequestsError } from "bereach/models/operations";

let value: WithdrawLinkedInInvitationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 702752,
  daily: {
    current: 501676,
    limit: 632539,
  },
  weekly: {
    current: 168975,
    limit: 960257,
  },
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                         | [operations.WithdrawLinkedInInvitationCode](../../models/operations/withdraw-linked-in-invitation-code.md)     | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `message`                                                                                                      | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `docs`                                                                                                         | *string*                                                                                                       | :heavy_minus_sign:                                                                                             | N/A                                                                                                            |
| `retryAfter`                                                                                                   | *number*                                                                                                       | :heavy_check_mark:                                                                                             | Seconds to wait before retrying.                                                                               |
| `daily`                                                                                                        | [operations.WithdrawLinkedInInvitationDaily](../../models/operations/withdraw-linked-in-invitation-daily.md)   | :heavy_check_mark:                                                                                             | Current and max daily usage (null if no daily cap).                                                            |
| `weekly`                                                                                                       | [operations.WithdrawLinkedInInvitationWeekly](../../models/operations/withdraw-linked-in-invitation-weekly.md) | :heavy_check_mark:                                                                                             | Current and max weekly usage (null if no weekly cap).                                                          |