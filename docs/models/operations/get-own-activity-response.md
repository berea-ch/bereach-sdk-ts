# GetOwnActivityResponse

Activity list

## Example Usage

```typescript
import { GetOwnActivityResponse } from "bereach/models/operations";

let value: GetOwnActivityResponse = {
  success: true,
  actor: "<value>",
  tabType: "COMMENTS",
  items: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  count: 308128,
  total: 998809,
  start: 97875,
  paginationToken: "<value>",
  creditsUsed: 859075,
  retryAfter: 650926,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `actor`                                                                                                                           | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | Always 'personal': user activity                                                                                                  |
| `tabType`                                                                                                                         | [operations.TabTypeResponse](../../models/operations/tab-type-response.md)                                                        | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `items`                                                                                                                           | *any*[]                                                                                                                           | :heavy_check_mark:                                                                                                                | Activity items: comments or reactions depending on tabType                                                                        |
| `count`                                                                                                                           | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `total`                                                                                                                           | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `start`                                                                                                                           | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `paginationToken`                                                                                                                 | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |