# ContactsGetFullMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsGetFullMeta } from "bereach/models/operations";

let value: ContactsGetFullMeta = {
  credits: {
    current: 6374.03,
    limit: 8227.06,
    remaining: 7467.7,
    percentage: 8148.29,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `credits`                                                                                 | [operations.ContactsGetFullCredits](../../models/operations/contacts-get-full-credits.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |