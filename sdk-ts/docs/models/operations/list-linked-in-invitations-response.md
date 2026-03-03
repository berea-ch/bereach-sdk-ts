# ListLinkedInInvitationsResponse

List of pending invitations

## Example Usage

```typescript
import { ListLinkedInInvitationsResponse } from "bereach/models/operations";

let value: ListLinkedInInvitationsResponse = {
  success: false,
  invitations: [],
  total: 4146.67,
  start: 982.38,
  count: 4733.6,
  creditsUsed: 657760,
  retryAfter: 372072,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `invitations`                                                                        | [operations.Invitation](../../models/operations/invitation.md)[]                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | Total number of pending invitations                                                  |
| `start`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `count`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |