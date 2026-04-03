# BatchScheduleResponse

Messages scheduled

## Example Usage

```typescript
import { BatchScheduleResponse } from "bereach/models/operations";

let value: BatchScheduleResponse = {
  success: true,
  scheduled: 657778,
  triggerFailures: 263832,
  scheduledSendAt: "<value>",
  staggerMinutes: 891784,
  lastSendAt: "<value>",
  creditsUsed: 596941,
  retryAfter: 382086,
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `success`                                                    | *true*                                                       | :heavy_check_mark:                                           | N/A                                                          |
| `scheduled`                                                  | *number*                                                     | :heavy_check_mark:                                           | Number of messages scheduled                                 |
| `triggerFailures`                                            | *number*                                                     | :heavy_check_mark:                                           | Number of cron trigger failures (messages reverted to draft) |
| `scheduledSendAt`                                            | *string*                                                     | :heavy_check_mark:                                           | ISO datetime for first send                                  |
| `staggerMinutes`                                             | *number*                                                     | :heavy_check_mark:                                           | Minutes between staggered sends (0 if single message)        |
| `lastSendAt`                                                 | *string*                                                     | :heavy_check_mark:                                           | ISO datetime when last staggered message will be sent        |
| `creditsUsed`                                                | *number*                                                     | :heavy_check_mark:                                           | Credits consumed (always 0 for workspace operations).        |
| `retryAfter`                                                 | *number*                                                     | :heavy_check_mark:                                           | Seconds to wait (always 0 for workspace operations).         |