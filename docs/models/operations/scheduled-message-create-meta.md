# ScheduledMessageCreateMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ScheduledMessageCreateMeta } from "bereach/models/operations";

let value: ScheduledMessageCreateMeta = {
  credits: {
    current: 4516.45,
    limit: 4774.8,
    remaining: 2947.65,
    percentage: 2271.68,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.ScheduledMessageCreateCredits](../../models/operations/scheduled-message-create-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |