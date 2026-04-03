# UpgradeWorkspaceAccountRequest

## Example Usage

```typescript
import { UpgradeWorkspaceAccountRequest } from "bereach/models/operations";

let value: UpgradeWorkspaceAccountRequest = {
  credentialsId: "<id>",
  action: "downgrade",
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credentialsId`                                                                                         | *string*                                                                                                | :heavy_check_mark:                                                                                      | LinkedIn credentials ID                                                                                 |
| `action`                                                                                                | [operations.UpgradeWorkspaceAccountAction](../../models/operations/upgrade-workspace-account-action.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |