# ContactsLogActivityMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsLogActivityMeta } from "bereach/models/operations";

let value: ContactsLogActivityMeta = {
  credits: {
    current: 7866.01,
    limit: 3.72,
    remaining: 7290.93,
    percentage: 18.37,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `credits`                                                                                         | [operations.ContactsLogActivityCredits](../../models/operations/contacts-log-activity-credits.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |