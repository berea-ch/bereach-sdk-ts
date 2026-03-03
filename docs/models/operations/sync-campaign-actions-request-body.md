# SyncCampaignActionsRequestBody

## Example Usage

```typescript
import { SyncCampaignActionsRequestBody } from "bereach/models/operations";

let value: SyncCampaignActionsRequestBody = {
  profiles: [
    {
      profile: "<value>",
      actions: [
        "reply",
      ],
    },
  ],
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `profiles`                                                                                          | [operations.SyncCampaignActionsProfile](../../models/operations/sync-campaign-actions-profile.md)[] | :heavy_check_mark:                                                                                  | Profiles and actions to mark as completed without performing them on LinkedIn.                      |