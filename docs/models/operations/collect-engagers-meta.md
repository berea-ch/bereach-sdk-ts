# CollectEngagersMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CollectEngagersMeta } from "bereach/models/operations";

let value: CollectEngagersMeta = {
  credits: {
    current: 7929.64,
    limit: 3530,
    remaining: 8906.51,
    percentage: 1748.25,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.CollectEngagersCredits](../../models/operations/collect-engagers-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |