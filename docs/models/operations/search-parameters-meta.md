# SearchParametersMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchParametersMeta } from "bereach/models/operations";

let value: SearchParametersMeta = {
  credits: {
    current: 6639.61,
    limit: 1660.42,
    remaining: 2764.57,
    percentage: 9393.57,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `credits`                                                                                  | [operations.SearchParametersCredits](../../models/operations/search-parameters-credits.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |