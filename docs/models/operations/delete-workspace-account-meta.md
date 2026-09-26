# DeleteWorkspaceAccountMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { DeleteWorkspaceAccountMeta } from "bereach/models/operations";

let value: DeleteWorkspaceAccountMeta = {
  credits: {
    current: 483.89,
    limit: 3917.96,
    remaining: 5997.16,
    percentage: 2064.39,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.DeleteWorkspaceAccountCredits](../../models/operations/delete-workspace-account-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |