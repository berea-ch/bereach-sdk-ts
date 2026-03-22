# ListSentInvitationsInvitation

## Example Usage

```typescript
import { ListSentInvitationsInvitation } from "bereach/models/operations";

let value: ListSentInvitationsInvitation = {
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
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `invitationId`                                              | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `invitationUrn`                                             | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `entityUrn`                                                 | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `sentAt`                                                    | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `message`                                                   | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetProfileId`                                           | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetFirstName`                                           | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetLastName`                                            | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `toMember`                                                  | [operations.ToMember](../../models/operations/to-member.md) | :heavy_check_mark:                                          | N/A                                                         |