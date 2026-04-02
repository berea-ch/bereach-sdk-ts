# GlobalActivitiesResponse

Activities list

## Example Usage

```typescript
import { GlobalActivitiesResponse } from "bereach/models/operations";

let value: GlobalActivitiesResponse = {
  success: true,
  activities: [
    {
      id: "<id>",
      type: "<value>",
      content: "<value>",
      metadata: "<value>",
      success: true,
      error: "<value>",
      createdAt: "1710054860835",
      contactId: "<id>",
      contactName: "<value>",
      contactLinkedinUrl: "https://impressive-guacamole.net",
    },
  ],
  pagination: {
    limit: 759457,
    offset: 69592,
    total: 854856,
  },
  creditsUsed: 119205,
  retryAfter: 319786,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `success`                                                                                        | *true*                                                                                           | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `activities`                                                                                     | [operations.GlobalActivitiesActivity](../../models/operations/global-activities-activity.md)[]   | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `pagination`                                                                                     | [operations.GlobalActivitiesPagination](../../models/operations/global-activities-pagination.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `creditsUsed`                                                                                    | *number*                                                                                         | :heavy_check_mark:                                                                               | Credits consumed by this call (always 0 for contacts queries).                                   |
| `retryAfter`                                                                                     | *number*                                                                                         | :heavy_check_mark:                                                                               | Seconds to wait before next call of the same type (always 0 for contacts queries).               |