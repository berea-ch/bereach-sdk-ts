# WithdrawInvitationRequest

## Example Usage

```typescript
import { WithdrawInvitationRequest } from "bereach/models/operations";

let value: WithdrawInvitationRequest = {
  invitationUrn: "<value>",
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `invitationUrn`                                                                 | *string*                                                                        | :heavy_check_mark:                                                              | Full invitation URN (e.g. urn:li:fs_relInvitation:123) or numeric invitation ID |