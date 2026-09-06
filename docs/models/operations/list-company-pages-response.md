# ListCompanyPagesResponse

List of managed company pages

## Example Usage

```typescript
import { ListCompanyPagesResponse } from "bereach/models/operations";

let value: ListCompanyPagesResponse = {
  success: true,
  pages: [],
  total: 820730,
  creditsUsed: 977500,
  retryAfter: 782496,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `pages`                                                                                                                                   | [operations.Page](../../models/operations/page.md)[]                                                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ListCompanyPagesMeta](../../models/operations/list-company-pages-meta.md)                                                     | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |