# ScheduledMessageCancelMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ScheduledMessageCancelMeta } from "bereach/models/operations";

let value: ScheduledMessageCancelMeta = {
  credits: {
    current: 8476,
    limit: null,
    remaining: 573.36,
    percentage: 996.39,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.ScheduledMessageCancelCredits](../../models/operations/scheduled-message-cancel-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |