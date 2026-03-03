# SyncCampaignActionsResponse

Actions marked as completed

## Example Usage

```typescript
import { SyncCampaignActionsResponse } from "bereach/models/operations";

let value: SyncCampaignActionsResponse = {
  success: true,
  synced: [
    {
      profile: "<value>",
      actions: {
        "key": true,
        "key1": false,
        "key2": false,
      },
    },
  ],
  creditsUsed: 780625,
  retryAfter: 735917,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |
| `synced`                                                                           | [operations.Synced](../../models/operations/synced.md)[]                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for campaign queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for campaign queries). |