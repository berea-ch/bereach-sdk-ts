# DiscardContactsResponse

Bulk update results

## Example Usage

```typescript
import { DiscardContactsResponse } from "bereach/models/operations";

let value: DiscardContactsResponse = {
  success: true,
  updated: 269197,
  skipped: 128967,
  errors: [
    "<value 1>",
  ],
  creditsUsed: 942638,
  retryAfter: 285556,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `updated`                                                                                                                         | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `skipped`                                                                                                                         | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `errors`                                                                                                                          | *string*[]                                                                                                                        | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |