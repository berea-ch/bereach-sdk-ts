# ContactsSearchResponse

Matching contacts. The row shape depends on `omitData`.

## Example Usage

```typescript
import { ContactsSearchResponse } from "bereach/models/operations";

let value: ContactsSearchResponse = {
  success: true,
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://snoopy-loyalty.com/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      hotScore: 620018,
      qualificationNotes: null,
      leadBrief: "<value>",
      notes: null,
      stageChangedAt: "<value>",
      profileUpdatedAt: "<value>",
      conversationUpdatedAt: null,
      tags: [],
      createdAt: "1711389342254",
      updatedAt: "1735662855998",
    },
  ],
  pagination: {
    limit: 162093,
    offset: 969474,
    total: 681961,
  },
  creditsUsed: 202349,
  retryAfter: 251282,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contacts`                                                                                                                                | *operations.ContactsUnion*                                                                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `pagination`                                                                                                                              | [operations.ContactsSearchPagination](../../models/operations/contacts-search-pagination.md)                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsSearchMeta](../../models/operations/contacts-search-meta.md)                                                          | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |