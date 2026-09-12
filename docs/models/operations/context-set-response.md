# ContextSetResponse

Context saved

## Example Usage

```typescript
import { ContextSetResponse } from "bereach/models/operations";

let value: ContextSetResponse = {
  success: true,
  entry: {
    id: "<id>",
    type: "<value>",
    label: "<value>",
    content: "<value>",
    scope: "<value>",
    updatedAt: "1735615987863",
  },
  creditsUsed: 959943,
  retryAfter: 447033,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `entry`                                                                                                                                   | [operations.ContextSetEntry](../../models/operations/context-set-entry.md)                                                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContextSetMeta](../../models/operations/context-set-meta.md)                                                                  | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |