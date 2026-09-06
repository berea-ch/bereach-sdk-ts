# ContactsCreateCampaignResponse

Campaign created

## Example Usage

```typescript
import { ContactsCreateCampaignResponse } from "bereach/models/operations";

let value: ContactsCreateCampaignResponse = {
  success: true,
  campaign: {
    id: "<id>",
    name: "<value>",
    description: "who weakly syringe",
    totalContacts: 803447,
    createdAt: "1708880302485",
    updatedAt: "1735646939588",
  },
  creditsUsed: 186859,
  retryAfter: 829714,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `campaign`                                                                                                                                | [operations.ContactsCreateCampaignCampaign](../../models/operations/contacts-create-campaign-campaign.md)                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ContactsCreateCampaignMeta](../../models/operations/contacts-create-campaign-meta.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |