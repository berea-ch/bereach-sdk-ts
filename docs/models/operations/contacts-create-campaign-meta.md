# ContactsCreateCampaignMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ContactsCreateCampaignMeta } from "bereach/models/operations";

let value: ContactsCreateCampaignMeta = {
  credits: {
    current: 2449.45,
    limit: 5161.76,
    remaining: 1709,
    percentage: 5865.84,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.ContactsCreateCampaignCredits](../../models/operations/contacts-create-campaign-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |