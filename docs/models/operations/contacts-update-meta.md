# ContactsUpdateMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsUpdateMeta } from "bereach/models/operations";

let value: ContactsUpdateMeta = {
  credits: {
    current: 3957.58,
    limit: 6172.34,
    remaining: 9503.86,
    percentage: 185.92,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | [operations.ContactsUpdateCredits](../../models/operations/contacts-update-credits.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |