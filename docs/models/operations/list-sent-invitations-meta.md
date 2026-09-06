# ListSentInvitationsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListSentInvitationsMeta } from "bereach/models/operations";

let value: ListSentInvitationsMeta = {
  credits: {
    current: 5625.46,
    limit: 4708,
    remaining: 2678.65,
    percentage: 8364.57,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `credits`                                                                                         | [operations.ListSentInvitationsCredits](../../models/operations/list-sent-invitations-credits.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |