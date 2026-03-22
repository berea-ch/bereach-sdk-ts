# ListSentInvitationsResponse

Sent invitations

## Example Usage

```typescript
import { ListSentInvitationsResponse } from "bereach/models/operations";

let value: ListSentInvitationsResponse = {
  success: true,
  invitations: [
    {
      invitationId: "<id>",
      invitationUrn: "<value>",
      entityUrn: "<value>",
      sentAt: "<value>",
      message: "<value>",
      targetProfileId: "<id>",
      targetFirstName: "<value>",
      targetLastName: "<value>",
      toMember: {
        name: "<value>",
        headline: null,
        profileUrl: "https://impassioned-dwell.name",
        profilePicture: "<value>",
        publicIdentifier: "<value>",
        profileUrn: "<value>",
      },
    },
  ],
  total: 750184,
  start: 933972,
  count: 245644,
  creditsUsed: 358618,
  retryAfter: 12504,
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                 | *true*                                                                                                    | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `invitations`                                                                                             | [operations.ListSentInvitationsInvitation](../../models/operations/list-sent-invitations-invitation.md)[] | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `total`                                                                                                   | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `start`                                                                                                   | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `count`                                                                                                   | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `creditsUsed`                                                                                             | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                      |
| `retryAfter`                                                                                              | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Seconds to wait before making another call of the same type. 0 means no wait needed.                      |