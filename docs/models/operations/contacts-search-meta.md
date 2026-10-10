# ContactsSearchMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsSearchMeta } from "bereach/models/operations";

let value: ContactsSearchMeta = {
  credits: {
    current: 2725.89,
    limit: 112.15,
    remaining: 4568.66,
    percentage: 5713.58,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | [operations.ContactsSearchCredits](../../models/operations/contacts-search-credits.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |