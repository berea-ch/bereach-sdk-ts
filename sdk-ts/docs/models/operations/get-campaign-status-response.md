# GetCampaignStatusResponse

Per-profile action completion status

## Example Usage

```typescript
import { GetCampaignStatusResponse } from "bereach/models/operations";

let value: GetCampaignStatusResponse = {
  success: false,
  profiles: [],
  creditsUsed: 554199,
  retryAfter: 762721,
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `success`                                                                                       | *boolean*                                                                                       | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `profiles`                                                                                      | [operations.GetCampaignStatusProfile](../../models/operations/get-campaign-status-profile.md)[] | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `creditsUsed`                                                                                   | *number*                                                                                        | :heavy_check_mark:                                                                              | Credits consumed by this call (always 0 for campaign queries).                                  |
| `retryAfter`                                                                                    | *number*                                                                                        | :heavy_check_mark:                                                                              | Seconds to wait before next call of the same type (always 0 for campaign queries).              |