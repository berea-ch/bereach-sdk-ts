# Invitation

## Example Usage

```typescript
import { Invitation } from "bereach/models/operations";

let value: Invitation = {
  invitationId: "<id>",
  sharedSecret: "<value>",
  entityUrn: "<value>",
  sentAt: null,
  message: "<value>",
  senderProfileId: "<id>",
  senderFirstName: "<value>",
  senderLastName: "<value>",
  fromMember: {
    name: "<value>",
    headline: "<value>",
    profileUrl: "https://glorious-gazebo.info",
    profilePicture: "<value>",
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `invitationId`                                                  | *string*                                                        | :heavy_check_mark:                                              | Invitation ID needed for accepting                              |
| `sharedSecret`                                                  | *string*                                                        | :heavy_check_mark:                                              | Shared secret needed for accepting                              |
| `entityUrn`                                                     | *string*                                                        | :heavy_check_mark:                                              | Full invitation URN                                             |
| `sentAt`                                                        | *string*                                                        | :heavy_check_mark:                                              | ISO 8601 timestamp when invitation was sent                     |
| `message`                                                       | *string*                                                        | :heavy_check_mark:                                              | Custom message included with the invitation                     |
| `senderProfileId`                                               | *string*                                                        | :heavy_check_mark:                                              | Sender's profile ID (pass to accept endpoint)                   |
| `senderFirstName`                                               | *string*                                                        | :heavy_check_mark:                                              | Sender's first name (pass to accept endpoint)                   |
| `senderLastName`                                                | *string*                                                        | :heavy_check_mark:                                              | Sender's last name (pass to accept endpoint)                    |
| `fromMember`                                                    | [operations.FromMember](../../models/operations/from-member.md) | :heavy_check_mark:                                              | Profile info of the person who sent the invitation              |