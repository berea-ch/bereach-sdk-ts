# MarkAllReadMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { MarkAllReadMeta } from "bereach/models/operations";

let value: MarkAllReadMeta = {
  credits: {
    current: 1354.64,
    limit: 2437.62,
    remaining: 6310.58,
    percentage: 8324.05,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `credits`                                                                         | [operations.MarkAllReadCredits](../../models/operations/mark-all-read-credits.md) | :heavy_check_mark:                                                                | N/A                                                                               |