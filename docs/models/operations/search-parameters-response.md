# SearchParametersResponse

Matching ids, or a hint explaining why there were none

## Example Usage

```typescript
import { SearchParametersResponse } from "bereach/models/operations";

let value: SearchParametersResponse = {
  success: true,
  items: [
    {
      id: "<id>",
      title: "<value>",
      type: "<value>",
    },
  ],
  count: 217655,
  aliasResolved: true,
  creditsUsed: 352637,
  retryAfter: 211549,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `items`                                                                                                                                   | [operations.SearchParametersItem](../../models/operations/search-parameters-item.md)[]                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hint`                                                                                                                                    | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | Present ONLY when nothing matched, and it says why rather than leaving an empty array to be read as an empty world.                       |
| `aliasResolved`                                                                                                                           | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | True when the curated alias map answered rather than LinkedIn.                                                                            |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchParametersMeta](../../models/operations/search-parameters-meta.md)                                                      | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |