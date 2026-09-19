# CreateWorkspaceInviteMeta2

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CreateWorkspaceInviteMeta2 } from "bereach/models/operations";

let value: CreateWorkspaceInviteMeta2 = {
  credits: {
    current: 5996.72,
    limit: 1947.66,
    remaining: 4991.55,
    percentage: 2023.54,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.CreateWorkspaceInviteCredits2](../../models/operations/create-workspace-invite-credits2.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |