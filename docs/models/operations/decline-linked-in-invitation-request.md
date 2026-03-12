# DeclineLinkedInInvitationRequest

## Example Usage

```typescript
import { DeclineLinkedInInvitationRequest } from "bereach/models/operations";

let value: DeclineLinkedInInvitationRequest = {
  invitationId: "<id>",
  sharedSecret: "<value>",
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `invitationId`                                                      | *string*                                                            | :heavy_check_mark:                                                  | Invitation ID from the list invitations endpoint                    |
| `sharedSecret`                                                      | *string*                                                            | :heavy_check_mark:                                                  | Shared secret / validation token from the list invitations endpoint |
| `senderProfileId`                                                   | *string*                                                            | :heavy_minus_sign:                                                  | Sender's profile ID (optional, improves accuracy)                   |