# ListActivitiesResponse

Contact activities

## Example Usage

```typescript
import { ListActivitiesResponse } from "bereach/models/operations";

let value: ListActivitiesResponse = {
  success: true,
  activities: [
    {
      id: "<id>",
      type: "<value>",
      content: "<value>",
      metadata: "<value>",
      createdAt: "1704668031544",
    },
  ],
  pagination: {
    limit: 225343,
    offset: 238207,
    total: 617335,
  },
  creditsUsed: 737729,
  retryAfter: 770821,
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `success`                                                                                    | *true*                                                                                       | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `activities`                                                                                 | [operations.ListActivitiesActivity](../../models/operations/list-activities-activity.md)[]   | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `pagination`                                                                                 | [operations.ListActivitiesPagination](../../models/operations/list-activities-pagination.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `creditsUsed`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | Credits consumed by this call (always 0 for contacts queries).                               |
| `retryAfter`                                                                                 | *number*                                                                                     | :heavy_check_mark:                                                                           | Seconds to wait before next call of the same type (always 0 for contacts queries).           |