# GetByUrlContact

## Example Usage

```typescript
import { GetByUrlContact } from "bereach/models/operations";

let value: GetByUrlContact = {
  id: "<id>",
  linkedinUrl: "https://stale-excess.com/",
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  name: "<value>",
  lifecycleStage: "<value>",
  hotScore: 731757,
  qualificationNotes: "<value>",
  notes: "<value>",
  stageChangedAt: null,
  profileData: "<value>",
  profileUpdatedAt: "<value>",
  conversationData: "<value>",
  conversationUpdatedAt: "<value>",
  outreachStatus: "<value>",
  lastContactedAt: "<value>",
  lastRepliedAt: "<value>",
  nextFollowUpAt: "<value>",
  doNotContact: false,
  tags: [
    "<value 1>",
    "<value 2>",
  ],
  createdAt: "1727651091354",
  updatedAt: "1735677724173",
  activities: [],
  campaigns: [
    {
      campaignId: "<id>",
      campaignName: "<value>",
      campaignStatus: "<value>",
      source: "<value>",
      sourceAngle: null,
      addedAt: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `id`                                                                            | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `linkedinUrl`                                                                   | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `profileUrn`                                                                    | *string*                                                                        | :heavy_check_mark:                                                              | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...)                        |
| `publicIdentifier`                                                              | *string*                                                                        | :heavy_check_mark:                                                              | LinkedIn vanity slug (e.g. joshuaau)                                            |
| `name`                                                                          | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `lifecycleStage`                                                                | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `hotScore`                                                                      | *number*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `qualificationNotes`                                                            | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `notes`                                                                         | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `stageChangedAt`                                                                | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `profileData`                                                                   | *any*                                                                           | :heavy_check_mark:                                                              | N/A                                                                             |
| `profileUpdatedAt`                                                              | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `conversationData`                                                              | *any*                                                                           | :heavy_check_mark:                                                              | N/A                                                                             |
| `conversationUpdatedAt`                                                         | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `outreachStatus`                                                                | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `lastContactedAt`                                                               | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `lastRepliedAt`                                                                 | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `nextFollowUpAt`                                                                | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `doNotContact`                                                                  | *boolean*                                                                       | :heavy_check_mark:                                                              | N/A                                                                             |
| `tags`                                                                          | *string*[]                                                                      | :heavy_check_mark:                                                              | N/A                                                                             |
| `createdAt`                                                                     | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `updatedAt`                                                                     | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `activities`                                                                    | [operations.GetByUrlActivity](../../models/operations/get-by-url-activity.md)[] | :heavy_check_mark:                                                              | N/A                                                                             |
| `campaigns`                                                                     | [operations.GetByUrlCampaign](../../models/operations/get-by-url-campaign.md)[] | :heavy_check_mark:                                                              | N/A                                                                             |