# CreateWorkspaceInviteResponse

Invite created or listed


## Supported Types

### `operations.ResponseBody1`

```typescript
const value: operations.ResponseBody1 = {
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

### `operations.ResponseBody2`

```typescript
const value: operations.ResponseBody2 = {
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

