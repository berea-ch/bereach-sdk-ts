# ScheduledMessageUpdateMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ScheduledMessageUpdateMeta } from "bereach/models/operations";

let value: ScheduledMessageUpdateMeta = {
  credits: {
    current: 2734.86,
    limit: 205.06,
    remaining: 7394.16,
    percentage: 6697.64,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.ScheduledMessageUpdateCredits](../../models/operations/scheduled-message-update-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |