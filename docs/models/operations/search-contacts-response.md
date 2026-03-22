# SearchContactsResponse

Matching contacts

## Example Usage

```typescript
import { SearchContactsResponse } from "bereach/models/operations";

let value: SearchContactsResponse = {
  success: true,
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://tepid-repeat.name/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      hotScore: 818944,
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
      nextFollowUpAt: null,
      doNotContact: true,
      tags: [
        "<value 1>",
        "<value 2>",
      ],
      createdAt: "1711845224090",
      updatedAt: "1735684500263",
      campaigns: [],
    },
  ],
  pagination: {
    limit: 324189,
    offset: 916325,
    total: 557453,
  },
  creditsUsed: 472889,
  retryAfter: 379221,
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `success`                                                                                    | *true*                                                                                       | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `contacts`                                                                                   | [operations.SearchContactsContact](../../models/operations/search-contacts-contact.md)[]     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `pagination`                                                                                 | [operations.SearchContactsPagination](../../models/operations/search-contacts-pagination.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `creditsUsed`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | Credits consumed by this call (always 0 for contacts queries).                               |
| `retryAfter`                                                                                 | *number*                                                                                     | :heavy_check_mark:                                                                           | Seconds to wait before next call of the same type (always 0 for contacts queries).           |