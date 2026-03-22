# ListInvitationsResponse

List of pending invitations

## Example Usage

```typescript
import { ListInvitationsResponse } from "bereach/models/operations";

let value: ListInvitationsResponse = {
  success: true,
  invitations: [],
  total: 8515.97,
  start: 8655.76,
  count: 9704.71,
  creditsUsed: 469595,
  retryAfter: 171143,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `success`                                                                                        | *true*                                                                                           | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `invitations`                                                                                    | [operations.ListInvitationsInvitation](../../models/operations/list-invitations-invitation.md)[] | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `total`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | Total number of pending invitations                                                              |
| `start`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `count`                                                                                          | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `creditsUsed`                                                                                    | *number*                                                                                         | :heavy_check_mark:                                                                               | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).             |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before making another call of the same type. 0 means no wait needed.             |