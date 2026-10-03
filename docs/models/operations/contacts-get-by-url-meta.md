# ContactsGetByUrlMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsGetByUrlMeta } from "bereach/models/operations";

let value: ContactsGetByUrlMeta = {
  credits: {
    current: 6026.82,
    limit: 5165.1,
    remaining: 309.51,
    percentage: 9946.15,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `credits`                                                                                    | [operations.ContactsGetByUrlCredits](../../models/operations/contacts-get-by-url-credits.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |