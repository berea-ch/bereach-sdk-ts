# ListInvitationsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListInvitationsMeta } from "bereach/models/operations";

let value: ListInvitationsMeta = {
  credits: {
    current: 296.87,
    limit: 4830.25,
    remaining: 9102.55,
    percentage: 8055.55,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.ListInvitationsCredits](../../models/operations/list-invitations-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |