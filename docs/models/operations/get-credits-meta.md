# GetCreditsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetCreditsMeta } from "bereach/models/operations";

let value: GetCreditsMeta = {
  credits: {
    current: 4231.99,
    limit: 1998.56,
    remaining: 8090.02,
    percentage: 3504.96,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `credits`                                                                               | [operations.GetCreditsMetaCredits](../../models/operations/get-credits-meta-credits.md) | :heavy_check_mark:                                                                      | N/A                                                                                     |