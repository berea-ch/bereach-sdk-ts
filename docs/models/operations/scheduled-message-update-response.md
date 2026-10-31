# ScheduledMessageUpdateResponse

Message updated

## Example Usage

```typescript
import { ScheduledMessageUpdateResponse } from "bereach/models/operations";

let value: ScheduledMessageUpdateResponse = {
  success: true,
  updated: 399343,
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

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `updated`                                                                                                                         | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | How many rows were edited.                                                                                                        |
| `ineligible`                                                                                                                      | [operations.ScheduledMessageUpdateIneligible](../../models/operations/scheduled-message-update-ineligible.md)[]                   | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |