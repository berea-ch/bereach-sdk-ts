# ContactsUpsertResponse

Contacts created or updated

## Example Usage

```typescript
import { ContactsUpsertResponse } from "bereach/models/operations";

let value: ContactsUpsertResponse = {
  success: true,
  results: {
    created: 80370,
    updated: 158766,
    skipped: 398554,
    errors: [],
  },
  contacts: [],
  creditsUsed: 501987,
  retryAfter: 579520,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `results`                                                                                                                                 | [operations.ContactsUpsertResults](../../models/operations/contacts-upsert-results.md)                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contacts`                                                                                                                                | [operations.ContactsUpsertContactResponseBody](../../models/operations/contacts-upsert-contact-response-body.md)[]                        | :heavy_check_mark:                                                                                                                        | The rows as written. No per-campaign fields: this route creates no campaign membership.                                                   |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsUpsertMeta](../../models/operations/contacts-upsert-meta.md)                                                          | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |