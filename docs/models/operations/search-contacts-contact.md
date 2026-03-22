# SearchContactsContact

## Example Usage

```typescript
import { SearchContactsContact } from "bereach/models/operations";

let value: SearchContactsContact = {
  id: "<id>",
  linkedinUrl: "https://yellow-massage.name/",
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  name: "<value>",
  lifecycleStage: "<value>",
  hotScore: 645028,
  qualificationNotes: "<value>",
  notes: "<value>",
  stageChangedAt: "<value>",
  profileData: "<value>",
  profileUpdatedAt: "<value>",
  conversationData: "<value>",
  conversationUpdatedAt: "<value>",
  outreachStatus: "<value>",
  lastContactedAt: "<value>",
  lastRepliedAt: null,
  nextFollowUpAt: "<value>",
  doNotContact: false,
  tags: [
    "<value 1>",
  ],
  createdAt: "1713798646838",
  updatedAt: "1735639880049",
  campaigns: [],
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `id`                                                                                       | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `linkedinUrl`                                                                              | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `profileUrn`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...)                                   |
| `publicIdentifier`                                                                         | *string*                                                                                   | :heavy_check_mark:                                                                         | LinkedIn vanity slug (e.g. joshuaau)                                                       |
| `name`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lifecycleStage`                                                                           | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `hotScore`                                                                                 | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `qualificationNotes`                                                                       | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `notes`                                                                                    | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `stageChangedAt`                                                                           | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `profileData`                                                                              | *any*                                                                                      | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `profileUpdatedAt`                                                                         | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `conversationData`                                                                         | *any*                                                                                      | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `conversationUpdatedAt`                                                                    | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `outreachStatus`                                                                           | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastContactedAt`                                                                          | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastRepliedAt`                                                                            | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `nextFollowUpAt`                                                                           | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `doNotContact`                                                                             | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `tags`                                                                                     | *string*[]                                                                                 | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `createdAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `updatedAt`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `campaigns`                                                                                | [operations.SearchContactsCampaign](../../models/operations/search-contacts-campaign.md)[] | :heavy_check_mark:                                                                         | N/A                                                                                        |