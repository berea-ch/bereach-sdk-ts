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

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `actor`                                                                                                                                   | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Always 'personal' — user activity                                                                                                         |
| `tabType`                                                                                                                                 | [operations.TabTypeResponse](../../models/operations/tab-type-response.md)                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | *any*[]                                                                                                                                   | :heavy_check_mark:                                                                                                                        | Activity items — comments or reactions depending on tabType                                                                               |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `start`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paginationToken`                                                                                                                         | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetOwnActivityMeta](../../models/operations/get-own-activity-meta.md)                                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |