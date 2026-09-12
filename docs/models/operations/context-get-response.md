# ContextGetResponse

Session snapshot

## Example Usage

```typescript
import { ContextGetResponse } from "bereach/models/operations";

let value: ContextGetResponse = {
  pipeline: {
    "key": 168068,
  },
  contexts: [
    {
      type: "<value>",
      label: "<value>",
      content: "<value>",
      scope: "<value>",
    },
  ],
  pendingDrafts: 890607,
  failedDrafts: 331104,
  pendingSentInvitations: 547720,
  activeAccount: {
    id: "<id>",
    name: "<value>",
    plan: "<value>",
    headline: null,
    status: "expired",
    isUnlimited: false,
    creditsLimit: 105412,
    creditsCount: 409333,
    simulateWrites: false,
    isCurrent: false,
  },
  accounts: [],
  activeCampaigns: [],
  recentEvents: [],
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | *any*                                                                                | :heavy_minus_sign:                                                                   | Credit balance and usage                                                             |
| `pipeline`                                                                           | Record<string, *number*>                                                             | :heavy_check_mark:                                                                   | People counts: fit, in the list, not a fit                                           |
| `contexts`                                                                           | [operations.Context](../../models/operations/context.md)[]                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `pendingDrafts`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `failedDrafts`                                                                       | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `pendingSentInvitations`                                                             | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `activeAccount`                                                                      | [operations.ActiveAccount](../../models/operations/active-account.md)                | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `accounts`                                                                           | [operations.ContextGetAccount](../../models/operations/context-get-account.md)[]     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `activeCampaigns`                                                                    | [operations.ActiveCampaign](../../models/operations/active-campaign.md)[]            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `sessionMeta`                                                                        | *any*                                                                                | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `onboardingState`                                                                    | *any*                                                                                | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `recentEvents`                                                                       | [operations.RecentEvent](../../models/operations/recent-event.md)[]                  | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `llmStatus`                                                                          | *string*                                                                             | :heavy_minus_sign:                                                                   | Set when the LLM circuit breaker has tripped for this credential.                    |
| `llmFirstTrippedAt`                                                                  | *number*                                                                             | :heavy_minus_sign:                                                                   | Epoch ms the breaker first tripped, so a caller can say how long it has been paused. |