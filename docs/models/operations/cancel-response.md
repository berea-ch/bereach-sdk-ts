# CancelResponse

Messages cancelled

## Example Usage

```typescript
import { CancelResponse } from "bereach/models/operations";

let value: CancelResponse = {
  success: true,
  cancelled: 265089,
  creditsUsed: 102989,
  retryAfter: 213534,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `success`                                             | *true*                                                | :heavy_check_mark:                                    | N/A                                                   |
| `cancelled`                                           | *number*                                              | :heavy_check_mark:                                    | N/A                                                   |
| `creditsUsed`                                         | *number*                                              | :heavy_check_mark:                                    | Credits consumed (always 0 for workspace operations). |
| `retryAfter`                                          | *number*                                              | :heavy_check_mark:                                    | Seconds to wait (always 0 for workspace operations).  |