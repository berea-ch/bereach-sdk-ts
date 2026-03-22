# BatchScheduleResponse

Messages scheduled

## Example Usage

```typescript
import { BatchScheduleResponse } from "bereach/models/operations";

let value: BatchScheduleResponse = {
  success: true,
  scheduled: 657778,
  creditsUsed: 263832,
  retryAfter: 891784,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `success`                                             | *true*                                                | :heavy_check_mark:                                    | N/A                                                   |
| `scheduled`                                           | *number*                                              | :heavy_check_mark:                                    | N/A                                                   |
| `creditsUsed`                                         | *number*                                              | :heavy_check_mark:                                    | Credits consumed (always 0 for workspace operations). |
| `retryAfter`                                          | *number*                                              | :heavy_check_mark:                                    | Seconds to wait (always 0 for workspace operations).  |