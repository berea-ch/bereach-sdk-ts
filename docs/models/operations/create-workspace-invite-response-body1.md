# CreateWorkspaceInviteResponseBody1

## Example Usage

```typescript
import { CreateWorkspaceInviteResponseBody1 } from "bereach/models/operations";

let value: CreateWorkspaceInviteResponseBody1 = {
  success: true,
  invite: {
    id: "<id>",
    email: "Briana.Renner@yahoo.com",
    name: "<value>",
    code: "<value>",
    maxUses: 113200,
    useCount: 348933,
    expiresAt: "1744363330649",
    createdAt: "1722545149857",
  },
  creditsUsed: 538260,
  retryAfter: 715490,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `invite`                                                                                                                                  | [operations.CreateWorkspaceInviteInvite1](../../models/operations/create-workspace-invite-invite1.md)                                     | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CreateWorkspaceInviteMeta1](../../models/operations/create-workspace-invite-meta1.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |