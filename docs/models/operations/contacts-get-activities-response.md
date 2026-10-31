# ContactsGetActivitiesResponse

Contact activities

## Example Usage

```typescript
import { ContactsGetActivitiesResponse } from "bereach/models/operations";

let value: ContactsGetActivitiesResponse = {
  success: true,
  activities: [],
  pagination: {
    limit: 628832,
    offset: 884622,
    total: 630748,
  },
  creditsUsed: 383898,
  retryAfter: 708407,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `activities`                                                                                                                      | [operations.ContactsGetActivitiesActivity](../../models/operations/contacts-get-activities-activity.md)[]                         | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `pagination`                                                                                                                      | [operations.ContactsGetActivitiesPagination](../../models/operations/contacts-get-activities-pagination.md)                       | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |