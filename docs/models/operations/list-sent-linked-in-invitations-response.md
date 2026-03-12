# ListSentLinkedInInvitationsResponse

Sent invitations

## Example Usage

```typescript
import { ListSentLinkedInInvitationsResponse } from "bereach/models/operations";

let value: ListSentLinkedInInvitationsResponse = {
  success: true,
  invitations: [
    "<value 1>",
  ],
  total: 338640,
  creditsUsed: 601283,
  retryAfter: 802837,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `invitations`                                                                        | *any*[]                                                                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |