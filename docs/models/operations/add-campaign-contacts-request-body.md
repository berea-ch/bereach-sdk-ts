# AddCampaignContactsRequestBody

## Example Usage

```typescript
import { AddCampaignContactsRequestBody } from "bereach/models/operations";

let value: AddCampaignContactsRequestBody = {
  contacts: [],
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `contacts`                                                                                          | [operations.AddCampaignContactsContact](../../models/operations/add-campaign-contacts-contact.md)[] | :heavy_check_mark:                                                                                  | Contacts to add (single or bulk)                                                                    |