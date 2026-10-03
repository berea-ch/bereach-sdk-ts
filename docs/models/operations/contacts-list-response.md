# ContactsListResponse

Campaign contacts

## Example Usage

```typescript
import { ContactsListResponse } from "bereach/models/operations";

let value: ContactsListResponse = {
  success: true,
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://dependable-fat.name/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      notes: "<value>",
      stageChangedAt: "<value>",
      profileUpdatedAt: "<value>",
      conversationUpdatedAt: null,
      tags: [
        "<value 1>",
        "<value 2>",
      ],
      createdAt: "1717712455945",
      updatedAt: "1735673502786",
      source: "<value>",
      sourceAngle: "<value>",
      addedAt: "<value>",
    },
  ],
  pagination: {
    limit: 203707,
    offset: 633082,
    total: 306599,
  },
  creditsUsed: 174437,
  retryAfter: 375309,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contacts`                                                                                                                                | [operations.ContactsListContact](../../models/operations/contacts-list-contact.md)[]                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `pagination`                                                                                                                              | [operations.ContactsListPagination](../../models/operations/contacts-list-pagination.md)                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsListMeta](../../models/operations/contacts-list-meta.md)                                                              | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |