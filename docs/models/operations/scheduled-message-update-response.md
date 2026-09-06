# ScheduledMessageUpdateResponse

Message updated

## Example Usage

```typescript
import { ScheduledMessageUpdateResponse } from "bereach/models/operations";

let value: ScheduledMessageUpdateResponse = {
  success: true,
  updated: [],
  ineligible: [
    {
      id: "<id>",
      currentStatus: "<value>",
    },
  ],
  creditsUsed: 124134,
  retryAfter: 998543,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `updated`                                                                                                                                 | [operations.Updated](../../models/operations/updated.md)[]                                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `ineligible`                                                                                                                              | [operations.Ineligible](../../models/operations/ineligible.md)[]                                                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ScheduledMessageUpdateMeta](../../models/operations/scheduled-message-update-meta.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |