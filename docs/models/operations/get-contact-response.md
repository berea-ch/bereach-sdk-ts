# GetContactResponse

Contact details

## Example Usage

```typescript
import { GetContactResponse } from "bereach/models/operations";

let value: GetContactResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://flowery-institute.name",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 21420,
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
    doNotContact: false,
    tags: [
      "<value 1>",
    ],
    createdAt: "1722553000165",
    updatedAt: "1735653230076",
    activities: [
      {
        id: "<id>",
        type: "<value>",
        content: null,
        metadata: null,
        createdAt: "1724460030824",
      },
    ],
    campaigns: [],
  },
  creditsUsed: 104661,
  retryAfter: 86742,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `contact`                                                                          | [operations.GetContactContact](../../models/operations/get-contact-contact.md)     | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |