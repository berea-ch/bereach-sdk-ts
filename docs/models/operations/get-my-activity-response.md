# GetMyActivityResponse

Activity list

## Example Usage

```typescript
import { GetMyActivityResponse } from "bereach/models/operations";

let value: GetMyActivityResponse = {
  success: true,
  actor: "<value>",
  tabType: "COMMENTS",
  items: [],
  count: 42848,
  total: 665316,
  start: 330032,
  paginationToken: "<value>",
  creditsUsed: 262016,
  retryAfter: 268083,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `actor`                                                                              | *string*                                                                             | :heavy_check_mark:                                                                   | 'personal' for user activity, 'company:{id}' for org activity                        |
| `tabType`                                                                            | [operations.TabTypeResponse](../../models/operations/tab-type-response.md)           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `items`                                                                              | *any*[]                                                                              | :heavy_check_mark:                                                                   | Activity items — comments or reactions depending on tabType                          |
| `count`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `start`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `paginationToken`                                                                    | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |