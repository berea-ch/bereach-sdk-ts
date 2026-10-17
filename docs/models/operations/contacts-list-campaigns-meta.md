# ContactsListCampaignsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsListCampaignsMeta } from "bereach/models/operations";

let value: ContactsListCampaignsMeta = {
  credits: {
    current: 1588.31,
    limit: 3839.88,
    remaining: 6752.39,
    percentage: 9247.43,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `credits`                                                                                             | [operations.ContactsListCampaignsCredits](../../models/operations/contacts-list-campaigns-credits.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |