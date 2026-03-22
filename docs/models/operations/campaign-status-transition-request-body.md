# CampaignStatusTransitionRequestBody

## Example Usage

```typescript
import { CampaignStatusTransitionRequestBody } from "bereach/models/operations";

let value: CampaignStatusTransitionRequestBody = {
  action: "activate",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `action`                                                                                                  | [operations.CampaignStatusTransitionAction](../../models/operations/campaign-status-transition-action.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `scheduledStartTime`                                                                                      | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `scheduledStopTime`                                                                                       | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `timezone`                                                                                                | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `runDays`                                                                                                 | *string*[]                                                                                                | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `dailyActionLimit`                                                                                        | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |