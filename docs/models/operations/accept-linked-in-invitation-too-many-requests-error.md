# AcceptLinkedInInvitationTooManyRequestsError

## Example Usage

```typescript
import { AcceptLinkedInInvitationTooManyRequestsError } from "bereach/models/operations";

let value: AcceptLinkedInInvitationTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 798003,
  daily: {
    current: 59424,
    limit: 976393,
  },
  weekly: {
    current: 884804,
    limit: 614050,
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                     | [operations.AcceptLinkedInInvitationCode](../../models/operations/accept-linked-in-invitation-code.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `message`                                                                                                  | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `docs`                                                                                                     | *string*                                                                                                   | :heavy_minus_sign:                                                                                         | N/A                                                                                                        |
| `retryAfter`                                                                                               | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Seconds to wait before retrying.                                                                           |
| `daily`                                                                                                    | [operations.AcceptLinkedInInvitationDaily](../../models/operations/accept-linked-in-invitation-daily.md)   | :heavy_check_mark:                                                                                         | Current and max daily usage (null if no daily cap).                                                        |
| `weekly`                                                                                                   | [operations.AcceptLinkedInInvitationWeekly](../../models/operations/accept-linked-in-invitation-weekly.md) | :heavy_check_mark:                                                                                         | Current and max weekly usage (null if no weekly cap).                                                      |