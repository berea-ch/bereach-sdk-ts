# GetOwnActivityMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetOwnActivityMeta } from "bereach/models/operations";

let value: GetOwnActivityMeta = {
  credits: {
    current: 70.59,
    limit: 1030.85,
    remaining: 2131.91,
    percentage: 5725.12,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `credits`                                                                               | [operations.GetOwnActivityCredits](../../models/operations/get-own-activity-credits.md) | :heavy_check_mark:                                                                      | N/A                                                                                     |