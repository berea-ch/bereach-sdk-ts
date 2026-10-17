# GetCreditsResponse

Credit balance for the workspace

## Example Usage

```typescript
import { GetCreditsResponse } from "bereach/models/operations";

let value: GetCreditsResponse = {
  success: true,
  credits: {
    current: 284087,
    limit: 104219,
    remaining: 714218,
    percentage: 1646.47,
    isUnlimited: true,
  },
  creditsUsed: 625600,
  retryAfter: 77573,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `credits`                                                                                                                                 | [operations.GetCreditsCredits](../../models/operations/get-credits-credits.md)                                                            | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetCreditsMeta](../../models/operations/get-credits-meta.md)                                                                  | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |