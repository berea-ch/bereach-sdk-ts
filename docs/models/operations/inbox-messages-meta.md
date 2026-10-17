# InboxMessagesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { InboxMessagesMeta } from "bereach/models/operations";

let value: InboxMessagesMeta = {
  credits: {
    current: 5477.52,
    limit: 6192.6,
    remaining: 8871.33,
    percentage: 8460.11,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.InboxMessagesCredits](../../models/operations/inbox-messages-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |