# CreateWorkspaceInviteMeta1

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CreateWorkspaceInviteMeta1 } from "bereach/models/operations";

let value: CreateWorkspaceInviteMeta1 = {
  credits: {
    current: 8476.78,
    limit: 7374.49,
    remaining: 9300.22,
    percentage: 8579.03,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.CreateWorkspaceInviteCredits1](../../models/operations/create-workspace-invite-credits1.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |