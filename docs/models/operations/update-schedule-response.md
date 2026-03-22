# UpdateScheduleResponse

Schedule updated

## Example Usage

```typescript
import { UpdateScheduleResponse } from "bereach/models/operations";

let value: UpdateScheduleResponse = {
  success: true,
  creditsUsed: 826381,
  retryAfter: 157710,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `success`                                             | *true*                                                | :heavy_check_mark:                                    | N/A                                                   |
| `creditsUsed`                                         | *number*                                              | :heavy_check_mark:                                    | Credits consumed (always 0 for workspace operations). |
| `retryAfter`                                          | *number*                                              | :heavy_check_mark:                                    | Seconds to wait (always 0 for workspace operations).  |