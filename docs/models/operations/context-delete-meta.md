# ContextDeleteMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContextDeleteMeta } from "bereach/models/operations";

let value: ContextDeleteMeta = {
  credits: {
    current: 720.62,
    limit: 2006.05,
    remaining: 0.08,
    percentage: 8201.13,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.ContextDeleteCredits](../../models/operations/context-delete-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |