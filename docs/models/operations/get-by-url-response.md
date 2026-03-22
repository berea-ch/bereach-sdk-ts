# GetByUrlResponse

Contact found

## Example Usage

```typescript
import { GetByUrlResponse } from "bereach/models/operations";

let value: GetByUrlResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://accomplished-hamburger.com",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 726565,
    qualificationNotes: "<value>",
    notes: "<value>",
    stageChangedAt: "<value>",
    profileData: "<value>",
    profileUpdatedAt: null,
    conversationData: "<value>",
    conversationUpdatedAt: "<value>",
    outreachStatus: "<value>",
    lastContactedAt: "<value>",
    lastRepliedAt: "<value>",
    nextFollowUpAt: "<value>",
    doNotContact: true,
    tags: [],
    createdAt: "1708634238334",
    updatedAt: "1735643142539",
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
  },
  creditsUsed: 469193,
  retryAfter: 967840,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `contact`                                                                          | [operations.GetByUrlContact](../../models/operations/get-by-url-contact.md)        | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |