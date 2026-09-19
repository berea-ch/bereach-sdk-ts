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
      notes: "<value>",
      stageChangedAt: null,
      profileUpdatedAt: "<value>",
      conversationUpdatedAt: null,
      tags: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      createdAt: "1725511710867",
      updatedAt: "1735611305614",
    },
  ],
  pagination: {
    limit: 76315,
    offset: 229444,
    total: 690471,
  },
  creditsUsed: 162093,
  retryAfter: 969474,
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