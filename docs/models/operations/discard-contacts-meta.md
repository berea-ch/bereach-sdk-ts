# DiscardContactsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { DiscardContactsMeta } from "bereach/models/operations";

let value: DiscardContactsMeta = {
  credits: {
    current: 8740.29,
    limit: 2595.24,
    remaining: 2325.75,
    percentage: 4771.88,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.DiscardContactsCredits](../../models/operations/discard-contacts-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |