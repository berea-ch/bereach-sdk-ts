# ListLinkedInInvitationsResponse

List of pending invitations

## Example Usage

```typescript
import { ListLinkedInInvitationsResponse } from "bereach/models/operations";

let value: ListLinkedInInvitationsResponse = {
  success: true,
  invitations: [
    {
      invitationId: "<id>",
      sharedSecret: "<value>",
      entityUrn: "<value>",
      sentAt: "<value>",
      message: "<value>",
      senderProfileId: null,
      senderFirstName: "<value>",
      senderLastName: "<value>",
      fromMember: {
        name: "<value>",
        headline: "<value>",
        profileUrl: "https://glorious-gazebo.info",
        profilePicture: "<value>",
      },
    },
  ],
  total: 2186.34,
  start: 8837.67,
  count: 5096.84,
  creditsUsed: 255224,
  retryAfter: 884487,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `invitations`                                                                        | [operations.Invitation](../../models/operations/invitation.md)[]                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | Total number of pending invitations                                                  |
| `start`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `count`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |