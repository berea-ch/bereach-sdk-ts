# GetLimitsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetLimitsMeta } from "bereach/models/operations";

let value: GetLimitsMeta = {
  credits: {
    current: 7619.72,
    limit: 4461.6,
    remaining: 6794.17,
    percentage: 4247.21,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `credits`                                                                    | [operations.GetLimitsCredits](../../models/operations/get-limits-credits.md) | :heavy_check_mark:                                                           | N/A                                                                          |