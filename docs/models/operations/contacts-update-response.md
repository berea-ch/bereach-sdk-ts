# ContactsUpdateResponse

Updated contact

## Example Usage

```typescript
import { ContactsUpdateResponse } from "bereach/models/operations";

let value: ContactsUpdateResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://agreeable-siege.net/",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 196317,
    qualificationNotes: "<value>",
    leadBrief: null,
    notes: "<value>",
    stageChangedAt: "<value>",
    profileUpdatedAt: "<value>",
    conversationUpdatedAt: "<value>",
    tags: [],
    createdAt: "1728034811590",
    updatedAt: "1735634187500",
  },
  creditsUsed: 567638,
  retryAfter: 772241,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contact`                                                                                                                                 | [operations.ContactsUpdateContact](../../models/operations/contacts-update-contact.md)                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsUpdateMeta](../../models/operations/contacts-update-meta.md)                                                          | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |