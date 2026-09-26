# ContactsGetActivitiesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsGetActivitiesMeta } from "bereach/models/operations";

let value: ContactsGetActivitiesMeta = {
  credits: {
    current: 4964.95,
    limit: 9645.59,
    remaining: 4140.47,
    percentage: 3404.75,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `credits`                                                                                             | [operations.ContactsGetActivitiesCredits](../../models/operations/contacts-get-activities-credits.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |