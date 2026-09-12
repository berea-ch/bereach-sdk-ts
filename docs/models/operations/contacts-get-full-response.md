# ContactsGetFullResponse

Contact details

## Example Usage

```typescript
import { ContactsGetFullResponse } from "bereach/models/operations";

let value: ContactsGetFullResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://livid-atrium.name/",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 189110,
    qualificationNotes: "<value>",
    leadBrief: "<value>",
    notes: "<value>",
    stageChangedAt: "<value>",
    profileUpdatedAt: "<value>",
    conversationUpdatedAt: "<value>",
    campaigns: [],
    tags: [
      "<value 1>",
    ],
    createdAt: "1722340564314",
    updatedAt: "1735612495720",
  },
  creditsUsed: 51359,
  retryAfter: 432915,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contact`                                                                                                                                 | [operations.ContactsGetFullContact](../../models/operations/contacts-get-full-contact.md)                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsGetFullMeta](../../models/operations/contacts-get-full-meta.md)                                                       | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |