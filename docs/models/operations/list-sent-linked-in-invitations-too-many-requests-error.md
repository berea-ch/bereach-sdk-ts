# ListSentLinkedInInvitationsTooManyRequestsError

## Example Usage

```typescript
import { ListSentLinkedInInvitationsTooManyRequestsError } from "bereach/models/operations";

let value: ListSentLinkedInInvitationsTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 882079,
  daily: null,
  weekly: {
    current: 225670,
    limit: 917993,
  },
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                            | [operations.ListSentLinkedInInvitationsCode](../../models/operations/list-sent-linked-in-invitations-code.md)     | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `message`                                                                                                         | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `docs`                                                                                                            | *string*                                                                                                          | :heavy_minus_sign:                                                                                                | N/A                                                                                                               |
| `retryAfter`                                                                                                      | *number*                                                                                                          | :heavy_check_mark:                                                                                                | Seconds to wait before retrying.                                                                                  |
| `daily`                                                                                                           | [operations.ListSentLinkedInInvitationsDaily](../../models/operations/list-sent-linked-in-invitations-daily.md)   | :heavy_check_mark:                                                                                                | Current and max daily usage (null if no daily cap).                                                               |
| `weekly`                                                                                                          | [operations.ListSentLinkedInInvitationsWeekly](../../models/operations/list-sent-linked-in-invitations-weekly.md) | :heavy_check_mark:                                                                                                | Current and max weekly usage (null if no weekly cap).                                                             |