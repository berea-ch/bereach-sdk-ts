# AgentSnapshotResponse

Session snapshot

## Example Usage

```typescript
import { AgentSnapshotResponse } from "bereach/models/operations";

let value: AgentSnapshotResponse = {
  credits: "<value>",
  pipeline: {
    "key": 840568,
  },
  contexts: [],
  pendingDrafts: 275539,
  failedDrafts: 166174,
  unreadDMs: 587383,
  pendingSentInvitations: 108855,
  activeAccount: {
    id: "<id>",
    name: "<value>",
    plan: "<value>",
    headline: "<value>",
    isUnlimited: false,
    creditsLimit: 152009,
    creditsCount: 375579,
    simulateWrites: true,
    isCurrent: true,
  },
  accounts: [
    {
      id: "<id>",
      name: "<value>",
      plan: "<value>",
      headline: "<value>",
      isUnlimited: false,
      creditsLimit: 974757,
      creditsCount: 304576,
      simulateWrites: false,
      isCurrent: true,
    },
  ],
  leadGenState: "<value>",
  outreachState: "<value>",
  activeCampaigns: [],
  campaignChecks: "<value>",
  sessionMeta: "<value>",
  onboardingState: "<value>",
  recentEvents: [],
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | *any*                                                                                  | :heavy_check_mark:                                                                     | Credit balance and usage                                                               |
| `pipeline`                                                                             | Record<string, *number*>                                                               | :heavy_check_mark:                                                                     | Contact counts by lifecycle stage                                                      |
| `contexts`                                                                             | [operations.Context](../../models/operations/context.md)[]                             | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pendingDrafts`                                                                        | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `failedDrafts`                                                                         | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `unreadDMs`                                                                            | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pendingSentInvitations`                                                               | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `activeAccount`                                                                        | [operations.ActiveAccount](../../models/operations/active-account.md)                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `accounts`                                                                             | [operations.AgentSnapshotAccount](../../models/operations/agent-snapshot-account.md)[] | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `leadGenState`                                                                         | *any*                                                                                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `outreachState`                                                                        | *any*                                                                                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `activeCampaigns`                                                                      | [operations.ActiveCampaign](../../models/operations/active-campaign.md)[]              | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `campaignChecks`                                                                       | *any*                                                                                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `sessionMeta`                                                                          | *any*                                                                                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `onboardingState`                                                                      | *any*                                                                                  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `recentEvents`                                                                         | [operations.RecentEvent](../../models/operations/recent-event.md)[]                    | :heavy_check_mark:                                                                     | N/A                                                                                    |