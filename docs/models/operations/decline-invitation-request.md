# DeclineInvitationRequest

## Example Usage

```typescript
import { DeclineInvitationRequest } from "bereach/models/operations";

let value: DeclineInvitationRequest = {
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