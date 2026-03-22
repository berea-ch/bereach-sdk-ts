# UpsertResponse

Contacts created or updated

## Example Usage

```typescript
import { UpsertResponse } from "bereach/models/operations";

let value: UpsertResponse = {
  success: true,
  results: {
    created: 715744,
    updated: 585087,
    skipped: 695185,
    errors: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://meaty-brush.name/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      hotScore: 254160,
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
      createdAt: "1729508779875",
      updatedAt: "1735650883389",
    },
  ],
  creditsUsed: 967558,
  retryAfter: 651402,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `results`                                                                                | [operations.UpsertResults](../../models/operations/upsert-results.md)                    | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `contacts`                                                                               | [operations.UpsertContactResponse](../../models/operations/upsert-contact-response.md)[] | :heavy_check_mark:                                                                       | Full contact objects with IDs for immediate use                                          |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed by this call (always 0 for contacts queries).                           |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before next call of the same type (always 0 for contacts queries).       |