# ContactsAddMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsAddMeta } from "bereach/models/operations";

let value: ContactsAddMeta = {
  credits: {
    current: 4415.53,
    limit: 688.27,
    remaining: 6305.59,
    percentage: 6070.39,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.ContactsAddCredits](../../models/operations/contacts-add-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |