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
      sentTime: 328835,
      message: "<value>",
      targetProfileId: "<id>",
      targetFirstName: "<value>",
      targetLastName: "<value>",
      toMember: {
        name: "<value>",
        headline: "<value>",
        profileUrl: "https://kaleidoscopic-deck.net",
        profilePicture: "<value>",
        publicIdentifier: "<value>",
        profileUrn: "<value>",
        memberId: "<id>",
      },
      invitationType: "<value>",
      mailboxItemId: "<id>",
      customMessage: true,
      unseen: true,
      inviterFollowingInvitee: true,
    },
  ],
  total: 95899,
  start: 235331,
  count: 644397,
  creditsUsed: 265127,
  retryAfter: 774772,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `invitations`                                                                                                                             | [operations.ListSentInvitationsInvitation](../../models/operations/list-sent-invitations-invitation.md)[]                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `start`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warning`                                                                                                                                 | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | Present ONLY when the list could not be confirmed complete. While it is present, absence from `invitations` proves nothing.               |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ListSentInvitationsMeta](../../models/operations/list-sent-invitations-meta.md)                                               | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |