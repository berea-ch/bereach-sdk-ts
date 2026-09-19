# ContactsLogActivityResponse

Activities logged

## Example Usage

```typescript
import { ContactsLogActivityResponse } from "bereach/models/operations";

let value: ContactsLogActivityResponse = {
  success: true,
  created: 794293,
  creditsUsed: 222960,
  retryAfter: 160466,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `created`                                                                                                                                 | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsLogActivityMeta](../../models/operations/contacts-log-activity-meta.md)                                               | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |