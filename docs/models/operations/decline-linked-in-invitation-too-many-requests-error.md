# DeclineLinkedInInvitationTooManyRequestsError

## Example Usage

```typescript
import { DeclineLinkedInInvitationTooManyRequestsError } from "bereach/models/operations";

let value: DeclineLinkedInInvitationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 911019,
  daily: {
    current: 314624,
    limit: 25029,
  },
  weekly: {
    current: 66248,
    limit: 581915,
  },
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `code`                                                                                                       | [operations.DeclineLinkedInInvitationCode](../../models/operations/decline-linked-in-invitation-code.md)     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `message`                                                                                                    | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `docs`                                                                                                       | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | N/A                                                                                                          |
| `retryAfter`                                                                                                 | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Seconds to wait before retrying.                                                                             |
| `daily`                                                                                                      | [operations.DeclineLinkedInInvitationDaily](../../models/operations/decline-linked-in-invitation-daily.md)   | :heavy_check_mark:                                                                                           | Current and max daily usage (null if no daily cap).                                                          |
| `weekly`                                                                                                     | [operations.DeclineLinkedInInvitationWeekly](../../models/operations/decline-linked-in-invitation-weekly.md) | :heavy_check_mark:                                                                                           | Current and max weekly usage (null if no weekly cap).                                                        |