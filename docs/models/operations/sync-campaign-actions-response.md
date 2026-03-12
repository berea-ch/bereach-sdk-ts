# SyncCampaignActionsResponse

Actions marked as completed

## Example Usage

```typescript
import { SyncCampaignActionsResponse } from "bereach/models/operations";

let value: SyncCampaignActionsResponse = {
  success: true,
  synced: [],
  creditsUsed: 872358,
  retryAfter: 780625,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `synced`                                                                           | [operations.Synced](../../models/operations/synced.md)[]                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for campaign queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for campaign queries). |