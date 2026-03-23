# GetCampaignCampaign

## Example Usage

```typescript
import { GetCampaignCampaign } from "bereach/models/operations";

let value: GetCampaignCampaign = {
  id: "<id>",
  name: "<value>",
  description: null,
  context: "<value>",
  type: "<value>",
  status: "<value>",
  totalContacts: 169435,
  createdAt: "1712818832631",
  updatedAt: "1735652263050",
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `id`                                                                                      | *string*                                                                                  | :heavy_check_mark:                                                                        | Campaign unique ID (nanoid). Use this as campaignSlug in API calls.                       |
| `name`                                                                                    | *string*                                                                                  | :heavy_check_mark:                                                                        | Human-readable campaign name.                                                             |
| `slug`                                                                                    | *string*                                                                                  | :heavy_minus_sign:                                                                        | URL-safe slug auto-generated from name.                                                   |
| `description`                                                                             | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `context`                                                                                 | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `type`                                                                                    | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `status`                                                                                  | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `totalContacts`                                                                           | *number*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `scheduledStartTime`                                                                      | *string*                                                                                  | :heavy_minus_sign:                                                                        | Daily start time (HH:MM)                                                                  |
| `scheduledStopTime`                                                                       | *string*                                                                                  | :heavy_minus_sign:                                                                        | Daily stop time (HH:MM)                                                                   |
| `timezone`                                                                                | *string*                                                                                  | :heavy_minus_sign:                                                                        | IANA timezone                                                                             |
| `runDays`                                                                                 | *string*[]                                                                                | :heavy_minus_sign:                                                                        | Days to run (e.g. ['monday','tuesday'])                                                   |
| `dailyActionLimit`                                                                        | *number*                                                                                  | :heavy_minus_sign:                                                                        | Max actions per day                                                                       |
| `startedAt`                                                                               | *string*                                                                                  | :heavy_minus_sign:                                                                        | When campaign was first started                                                           |
| `completedAt`                                                                             | *string*                                                                                  | :heavy_minus_sign:                                                                        | When campaign was completed                                                               |
| `stageCounts`                                                                             | [operations.GetCampaignStageCounts](../../models/operations/get-campaign-stage-counts.md) | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `createdAt`                                                                               | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `updatedAt`                                                                               | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |