# CreateWorkspaceInviteRequest

## Example Usage

```typescript
import { CreateWorkspaceInviteRequest } from "bereach/models/operations";

let value: CreateWorkspaceInviteRequest = {
  action: "list",
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `action`                                                                                            | [operations.CreateWorkspaceInviteAction](../../models/operations/create-workspace-invite-action.md) | :heavy_check_mark:                                                                                  | "create" to make a new invite, "list" to get existing                                               |
| `email`                                                                                             | *string*                                                                                            | :heavy_minus_sign:                                                                                  | Invitee email (sends invite email)                                                                  |
| `name`                                                                                              | *string*                                                                                            | :heavy_minus_sign:                                                                                  | Invitee name                                                                                        |
| `maxUses`                                                                                           | *number*                                                                                            | :heavy_minus_sign:                                                                                  | Max times code can be used                                                                          |