# GetCampaignStatusRequest

## Example Usage

```typescript
import { GetCampaignStatusRequest } from "bereach/models/operations";

let value: GetCampaignStatusRequest = {
  campaignSlug: "<value>",
  body: {
    profiles: [
      "<value 1>",
      "<value 2>",
    ],
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `campaignSlug`                                                                                         | *string*                                                                                               | :heavy_check_mark:                                                                                     | Campaign identifier                                                                                    |
| `body`                                                                                                 | [operations.GetCampaignStatusRequestBody](../../models/operations/get-campaign-status-request-body.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |