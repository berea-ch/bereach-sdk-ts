# GetCampaignStatsResponse

Aggregate campaign statistics

## Example Usage

```typescript
import { GetCampaignStatsResponse } from "bereach/models/operations";

let value: GetCampaignStatsResponse = {
  success: true,
  stats: {
    "key": 3159.33,
    "key1": 9311.55,
  },
  totalProfiles: 840767,
  creditsUsed: 890227,
  retryAfter: 821228,
};
```

## Fields

| Field                                                                                                                                 | Type                                                                                                                                  | Required                                                                                                                              | Description                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                             | *true*                                                                                                                                | :heavy_check_mark:                                                                                                                    | N/A                                                                                                                                   |
| `stats`                                                                                                                               | Record<string, *number*>                                                                                                              | :heavy_check_mark:                                                                                                                    | Per-action-type counts (e.g. message: 45, reply: 120)                                                                                 |
| `totalProfiles`                                                                                                                       | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Unique profiles processed in this campaign                                                                                            |
| `creditsUsed`                                                                                                                         | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Total credits consumed by this campaign (sum of action counts). Also serves as the per-call creditsUsed (always 0 for this endpoint). |
| `retryAfter`                                                                                                                          | *number*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Seconds to wait before next call of the same type (always 0 for campaign queries).                                                    |