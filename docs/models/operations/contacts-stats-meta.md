# ContactsStatsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsStatsMeta } from "bereach/models/operations";

let value: ContactsStatsMeta = {
  credits: {
    current: 9956.95,
    limit: 2738.62,
    remaining: 794.09,
    percentage: 6456.67,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.ContactsStatsCredits](../../models/operations/contacts-stats-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |