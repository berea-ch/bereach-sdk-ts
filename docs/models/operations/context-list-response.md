# ContextListResponse

Context entries

## Example Usage

```typescript
import { ContextListResponse } from "bereach/models/operations";

let value: ContextListResponse = {
  success: true,
  entries: [],
  total: 65628,
  hasMore: false,
  creditsUsed: 126269,
  retryAfter: 661447,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `entries`                                                                                                                                 | [operations.ContextListEntry](../../models/operations/context-list-entry.md)[]                                                            | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total matching entries                                                                                                                    |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContextListMeta](../../models/operations/context-list-meta.md)                                                                | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |