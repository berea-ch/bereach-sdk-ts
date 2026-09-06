# ResponseBody2

## Example Usage

```typescript
import { ResponseBody2 } from "bereach/models/operations";

let value: ResponseBody2 = {
  success: true,
  invites: [],
  workspace: {
    tier: "<value>",
    proSeatsIncluded: 669472,
    proSeatsUsed: 313584,
  },
  creditsUsed: 512221,
  retryAfter: 494422,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `invites`                                                                                                                                 | [operations.Invite2](../../models/operations/invite2.md)[]                                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `workspace`                                                                                                                               | [operations.Workspace](../../models/operations/workspace.md)                                                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CreateWorkspaceInviteMeta2](../../models/operations/create-workspace-invite-meta2.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |