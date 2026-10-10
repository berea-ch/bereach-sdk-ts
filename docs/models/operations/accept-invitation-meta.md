# AcceptInvitationMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { AcceptInvitationMeta } from "bereach/models/operations";

let value: AcceptInvitationMeta = {
  credits: {
    current: 7486.59,
    limit: 8679.36,
    remaining: 8581.3,
    percentage: 7986.02,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `credits`                                                                                  | [operations.AcceptInvitationCredits](../../models/operations/accept-invitation-credits.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |