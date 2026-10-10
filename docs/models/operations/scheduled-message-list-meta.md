# ScheduledMessageListMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ScheduledMessageListMeta } from "bereach/models/operations";

let value: ScheduledMessageListMeta = {
  credits: {
    current: 8346.93,
    limit: 7547.1,
    remaining: 6726.24,
    percentage: 294.1,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `credits`                                                                                           | [operations.ScheduledMessageListCredits](../../models/operations/scheduled-message-list-credits.md) | :heavy_check_mark:                                                                                  | N/A                                                                                                 |