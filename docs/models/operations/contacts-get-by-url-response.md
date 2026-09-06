# ContactsGetByUrlResponse

Contact found

## Example Usage

```typescript
import { ContactsGetByUrlResponse } from "bereach/models/operations";

let value: ContactsGetByUrlResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://scented-turret.com",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    hotScore: 548166,
    qualificationNotes: "<value>",
    leadBrief: "<value>",
    notes: null,
    stageChangedAt: "<value>",
    profileUpdatedAt: "<value>",
    conversationUpdatedAt: "<value>",
    campaigns: [],
    tags: [
      "<value 1>",
      "<value 2>",
    ],
    createdAt: "1727721980580",
    updatedAt: "1735642334279",
  },
  creditsUsed: 593450,
  retryAfter: 254372,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contact`                                                                                                                                 | [operations.ContactsGetByUrlContact](../../models/operations/contacts-get-by-url-contact.md)                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsGetByUrlMeta](../../models/operations/contacts-get-by-url-meta.md)                                                    | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |