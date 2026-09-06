# ResponseBody1

## Example Usage

```typescript
import { ResponseBody1 } from "bereach/models/operations";

let value: ResponseBody1 = {
  success: true,
  invite: {
    id: "<id>",
    email: "Ellis48@hotmail.com",
    name: null,
    code: "<value>",
    maxUses: 949705,
    useCount: 867079,
    expiresAt: "1745675942128",
    createdAt: "1732496019313",
  },
  creditsUsed: 53216,
  retryAfter: 310061,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `invite`                                                                                                                                  | [operations.Invite1](../../models/operations/invite1.md)                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CreateWorkspaceInviteMeta1](../../models/operations/create-workspace-invite-meta1.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |