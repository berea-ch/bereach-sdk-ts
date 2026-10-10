# CreateWorkspaceInviteResponseBody2

## Example Usage

```typescript
import { CreateWorkspaceInviteResponseBody2 } from "bereach/models/operations";

let value: CreateWorkspaceInviteResponseBody2 = {
  success: true,
  invites: [
    {
      id: "<id>",
      email: "Marlon49@gmail.com",
      name: "<value>",
      code: "<value>",
      maxUses: 511240,
      useCount: 257969,
      expiresAt: "1747732612764",
      createdAt: "1719599439104",
    },
  ],
  workspace: {
    tier: "<value>",
    proSeatsIncluded: 455311,
    proSeatsUsed: 101401,
  },
  creditsUsed: 396869,
  retryAfter: 115536,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `invites`                                                                                                                                 | [operations.CreateWorkspaceInviteInvite2](../../models/operations/create-workspace-invite-invite2.md)[]                                   | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `workspace`                                                                                                                               | [operations.Workspace](../../models/operations/workspace.md)                                                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CreateWorkspaceInviteMeta2](../../models/operations/create-workspace-invite-meta2.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |