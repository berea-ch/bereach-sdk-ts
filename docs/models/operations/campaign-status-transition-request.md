# CampaignStatusTransitionRequest

## Example Usage

```typescript
import { CampaignStatusTransitionRequest } from "bereach/models/operations";

let value: CampaignStatusTransitionRequest = {
  campaignId: "<id>",
  body: {
    action: "reset",
  },
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | Campaign ID                                                                                                          |
| `body`                                                                                                               | [operations.CampaignStatusTransitionRequestBody](../../models/operations/campaign-status-transition-request-body.md) | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |