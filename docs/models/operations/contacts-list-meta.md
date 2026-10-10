# ContactsListMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsListMeta } from "bereach/models/operations";

let value: ContactsListMeta = {
  credits: {
    current: 1541.59,
    limit: 9963.12,
    remaining: 2749.65,
    percentage: 2334.03,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.ContactsListCredits](../../models/operations/contacts-list-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |