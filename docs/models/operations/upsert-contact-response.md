# UpsertContactResponse

## Example Usage

```typescript
import { UpsertContactResponse } from "bereach/models/operations";

let value: UpsertContactResponse = {
  id: "<id>",
  linkedinUrl: "https://untrue-commodity.biz/",
  profileUrn: null,
  publicIdentifier: null,
  name: "<value>",
  lifecycleStage: "<value>",
  hotScore: 387437,
  qualificationNotes: "<value>",
  notes: "<value>",
  stageChangedAt: "<value>",
  profileData: "<value>",
  profileUpdatedAt: "<value>",
  conversationData: "<value>",
  conversationUpdatedAt: "<value>",
  outreachStatus: "<value>",
  lastContactedAt: "<value>",
  lastRepliedAt: "<value>",
  nextFollowUpAt: "<value>",
  doNotContact: true,
  tags: [
    "<value 1>",
  ],
  createdAt: "1733628000622",
  updatedAt: "1735628548853",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `id`                                                     | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `linkedinUrl`                                            | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `profileUrn`                                             | *string*                                                 | :heavy_check_mark:                                       | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) |
| `publicIdentifier`                                       | *string*                                                 | :heavy_check_mark:                                       | LinkedIn vanity slug (e.g. joshuaau)                     |
| `name`                                                   | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `lifecycleStage`                                         | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `hotScore`                                               | *number*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `qualificationNotes`                                     | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `notes`                                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `stageChangedAt`                                         | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `profileData`                                            | *any*                                                    | :heavy_check_mark:                                       | N/A                                                      |
| `profileUpdatedAt`                                       | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `conversationData`                                       | *any*                                                    | :heavy_check_mark:                                       | N/A                                                      |
| `conversationUpdatedAt`                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `outreachStatus`                                         | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `lastContactedAt`                                        | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `lastRepliedAt`                                          | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `nextFollowUpAt`                                         | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `doNotContact`                                           | *boolean*                                                | :heavy_check_mark:                                       | N/A                                                      |
| `tags`                                                   | *string*[]                                               | :heavy_check_mark:                                       | N/A                                                      |
| `createdAt`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `updatedAt`                                              | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |