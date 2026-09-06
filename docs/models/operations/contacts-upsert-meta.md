# ContactsUpsertMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsUpsertMeta } from "bereach/models/operations";

let value: ContactsUpsertMeta = {
  credits: {
    current: 8667.19,
    limit: 3114.52,
    remaining: 3469.01,
    percentage: 1789.17,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | [operations.ContactsUpsertCredits](../../models/operations/contacts-upsert-credits.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |