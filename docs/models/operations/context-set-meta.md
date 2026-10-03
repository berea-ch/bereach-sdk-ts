# ContextSetMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContextSetMeta } from "bereach/models/operations";

let value: ContextSetMeta = {
  credits: {
    current: 8678.03,
    limit: null,
    remaining: 5197.7,
    percentage: 8141.58,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `credits`                                                                      | [operations.ContextSetCredits](../../models/operations/context-set-credits.md) | :heavy_check_mark:                                                             | N/A                                                                            |