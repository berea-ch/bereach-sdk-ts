# ContextListMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContextListMeta } from "bereach/models/operations";

let value: ContextListMeta = {
  credits: {
    current: 6952.1,
    limit: 5788.04,
    remaining: 5715.51,
    percentage: 4760.38,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.ContextListCredits](../../models/operations/context-list-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |