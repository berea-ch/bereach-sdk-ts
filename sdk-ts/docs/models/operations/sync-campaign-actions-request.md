# SyncCampaignActionsRequest

## Example Usage

```typescript
import { SyncCampaignActionsRequest } from "bereach/models/operations";

let value: SyncCampaignActionsRequest = {
  campaignSlug: "<value>",
  body: {
    profiles: [
      {
        profile: "<value>",
        actions: [
          "reply",
        ],
      },
    ],
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `campaignSlug`                                                                                             | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Campaign identifier                                                                                        |
| `body`                                                                                                     | [operations.SyncCampaignActionsRequestBody](../../models/operations/sync-campaign-actions-request-body.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |