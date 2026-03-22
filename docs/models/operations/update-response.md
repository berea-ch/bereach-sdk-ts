# UpdateResponse

Updated contact

## Example Usage

```typescript
import { UpdateResponse } from "bereach/models/operations";

let value: UpdateResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://vivid-devastation.net",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 706615,
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
      "<value 2>",
    ],
    createdAt: "1709508483235",
    updatedAt: "1735651752331",
  },
  creditsUsed: 478941,
  retryAfter: 483854,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `contact`                                                                          | [operations.UpdateContact](../../models/operations/update-contact.md)              | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |