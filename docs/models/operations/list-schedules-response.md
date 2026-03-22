# ListSchedulesResponse

Cron schedules

## Example Usage

```typescript
import { ListSchedulesResponse } from "bereach/models/operations";

let value: ListSchedulesResponse = {
  success: true,
  schedules: [],
  creditsUsed: 290463,
  retryAfter: 200381,
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `success`                                                    | *true*                                                       | :heavy_check_mark:                                           | N/A                                                          |
| `schedules`                                                  | [operations.Schedule](../../models/operations/schedule.md)[] | :heavy_check_mark:                                           | N/A                                                          |
| `creditsUsed`                                                | *number*                                                     | :heavy_check_mark:                                           | Credits consumed (always 0 for workspace operations).        |
| `retryAfter`                                                 | *number*                                                     | :heavy_check_mark:                                           | Seconds to wait (always 0 for workspace operations).         |