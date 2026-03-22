# GetContactContact

## Example Usage

```typescript
import { GetContactContact } from "bereach/models/operations";

let value: GetContactContact = {
  id: "<id>",
  linkedinUrl: "https://wrong-hygienic.info",
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  name: "<value>",
  lifecycleStage: "<value>",
  hotScore: 734826,
  qualificationNotes: "<value>",
  notes: "<value>",
  stageChangedAt: "<value>",
  profileData: "<value>",
  profileUpdatedAt: "<value>",
  conversationData: null,
  conversationUpdatedAt: "<value>",
  outreachStatus: "<value>",
  lastContactedAt: "<value>",
  lastRepliedAt: "<value>",
  nextFollowUpAt: "<value>",
  doNotContact: false,
  tags: [],
  createdAt: "1731832580788",
  updatedAt: "1735629410126",
  activities: [
    {
      id: "<id>",
      type: "<value>",
      content: null,
      metadata: null,
      createdAt: "1724460030824",
    },
  ],
  campaigns: [
    {
      campaignId: "<id>",
      campaignName: "<value>",
      campaignStatus: "<value>",
      source: "<value>",
      sourceAngle: "<value>",
      addedAt: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `id`                                                                               | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `linkedinUrl`                                                                      | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `profileUrn`                                                                       | *string*                                                                           | :heavy_check_mark:                                                                 | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...)                           |
| `publicIdentifier`                                                                 | *string*                                                                           | :heavy_check_mark:                                                                 | LinkedIn vanity slug (e.g. joshuaau)                                               |
| `name`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `lifecycleStage`                                                                   | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `hotScore`                                                                         | *number*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `qualificationNotes`                                                               | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `notes`                                                                            | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `stageChangedAt`                                                                   | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `profileData`                                                                      | *any*                                                                              | :heavy_check_mark:                                                                 | N/A                                                                                |
| `profileUpdatedAt`                                                                 | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `conversationData`                                                                 | *any*                                                                              | :heavy_check_mark:                                                                 | N/A                                                                                |
| `conversationUpdatedAt`                                                            | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `outreachStatus`                                                                   | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `lastContactedAt`                                                                  | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `lastRepliedAt`                                                                    | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `nextFollowUpAt`                                                                   | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `doNotContact`                                                                     | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |
| `tags`                                                                             | *string*[]                                                                         | :heavy_check_mark:                                                                 | N/A                                                                                |
| `createdAt`                                                                        | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `updatedAt`                                                                        | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `activities`                                                                       | [operations.GetContactActivity](../../models/operations/get-contact-activity.md)[] | :heavy_check_mark:                                                                 | N/A                                                                                |
| `campaigns`                                                                        | [operations.GetContactCampaign](../../models/operations/get-contact-campaign.md)[] | :heavy_check_mark:                                                                 | N/A                                                                                |