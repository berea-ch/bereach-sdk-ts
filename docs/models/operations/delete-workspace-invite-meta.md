# DeleteWorkspaceInviteMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { DeleteWorkspaceInviteMeta } from "bereach/models/operations";

let value: DeleteWorkspaceInviteMeta = {
  credits: {
    current: 8862.66,
    limit: 604.62,
    remaining: 1054.28,
    percentage: 6656.28,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `credits`                                                                                             | [operations.DeleteWorkspaceInviteCredits](../../models/operations/delete-workspace-invite-credits.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |