# UpgradeWorkspaceAccountMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UpgradeWorkspaceAccountMeta } from "bereach/models/operations";

let value: UpgradeWorkspaceAccountMeta = {
  credits: {
    current: 3017.96,
    limit: 6241.07,
    remaining: 2387.65,
    percentage: 1652.09,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                                 | [operations.UpgradeWorkspaceAccountCredits](../../models/operations/upgrade-workspace-account-credits.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |