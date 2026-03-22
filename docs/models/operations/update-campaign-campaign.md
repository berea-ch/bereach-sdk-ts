# UpdateCampaignCampaign

## Example Usage

```typescript
import { UpdateCampaignCampaign } from "bereach/models/operations";

let value: UpdateCampaignCampaign = {
  id: "<id>",
  name: "<value>",
  description: "rapidly kindheartedly lowball oh whereas huzzah motor last how",
  context: "<value>",
  type: "<value>",
  status: "<value>",
  totalContacts: 880509,
  createdAt: "1714205872030",
  updatedAt: "1735622021121",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `name`                                                                                          | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `description`                                                                                   | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `context`                                                                                       | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `type`                                                                                          | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `status`                                                                                        | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `totalContacts`                                                                                 | *number*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `scheduledStartTime`                                                                            | *string*                                                                                        | :heavy_minus_sign:                                                                              | Daily start time (HH:MM)                                                                        |
| `scheduledStopTime`                                                                             | *string*                                                                                        | :heavy_minus_sign:                                                                              | Daily stop time (HH:MM)                                                                         |
| `timezone`                                                                                      | *string*                                                                                        | :heavy_minus_sign:                                                                              | IANA timezone                                                                                   |
| `runDays`                                                                                       | *string*[]                                                                                      | :heavy_minus_sign:                                                                              | Days to run (e.g. ['monday','tuesday'])                                                         |
| `dailyActionLimit`                                                                              | *number*                                                                                        | :heavy_minus_sign:                                                                              | Max actions per day                                                                             |
| `startedAt`                                                                                     | *string*                                                                                        | :heavy_minus_sign:                                                                              | When campaign was first started                                                                 |
| `completedAt`                                                                                   | *string*                                                                                        | :heavy_minus_sign:                                                                              | When campaign was completed                                                                     |
| `stageCounts`                                                                                   | [operations.UpdateCampaignStageCounts](../../models/operations/update-campaign-stage-counts.md) | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `createdAt`                                                                                     | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `updatedAt`                                                                                     | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |