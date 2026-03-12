# ListLinkedInInvitationsTooManyRequestsError

## Example Usage

```typescript
import { ListLinkedInInvitationsTooManyRequestsError } from "bereach/models/operations";

let value: ListLinkedInInvitationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 89153,
  daily: {
    current: 669499,
    limit: 919384,
  },
  weekly: {
    current: 852763,
    limit: 285747,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                   | [operations.ListLinkedInInvitationsCode](../../models/operations/list-linked-in-invitations-code.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `message`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `docs`                                                                                                   | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `retryAfter`                                                                                             | *number*                                                                                                 | :heavy_check_mark:                                                                                       | Seconds to wait before retrying.                                                                         |
| `daily`                                                                                                  | [operations.ListLinkedInInvitationsDaily](../../models/operations/list-linked-in-invitations-daily.md)   | :heavy_check_mark:                                                                                       | Current and max daily usage (null if no daily cap).                                                      |
| `weekly`                                                                                                 | [operations.ListLinkedInInvitationsWeekly](../../models/operations/list-linked-in-invitations-weekly.md) | :heavy_check_mark:                                                                                       | Current and max weekly usage (null if no weekly cap).                                                    |