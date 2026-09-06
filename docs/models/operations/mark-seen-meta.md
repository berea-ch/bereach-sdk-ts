# MarkSeenMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { MarkSeenMeta } from "bereach/models/operations";

let value: MarkSeenMeta = {
  credits: {
    current: 7576.58,
    limit: 9222.89,
    remaining: 6225.6,
    percentage: 1550.28,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `credits`                                                                  | [operations.MarkSeenCredits](../../models/operations/mark-seen-credits.md) | :heavy_check_mark:                                                         | N/A                                                                        |