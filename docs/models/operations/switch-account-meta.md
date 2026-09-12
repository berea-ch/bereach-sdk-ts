# SwitchAccountMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SwitchAccountMeta } from "bereach/models/operations";

let value: SwitchAccountMeta = {
  credits: {
    current: 2667.66,
    limit: 1760.66,
    remaining: 4561.25,
    percentage: 6572.72,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.SwitchAccountCredits](../../models/operations/switch-account-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |