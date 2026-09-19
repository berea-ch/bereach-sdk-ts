# ContactsUpdateRequest

## Example Usage

```typescript
import { ContactsUpdateRequest } from "bereach/models/operations";

let value: ContactsUpdateRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                        | *string*                                                                                            | :heavy_minus_sign:                                                                                  | Scopes the write to one list. Omit it: a chat turn writes to the list of the conversation it is in. |
| `id`                                                                                                | *string*                                                                                            | :heavy_check_mark:                                                                                  | Contact ID                                                                                          |
| `body`                                                                                              | [operations.ContactsUpdateRequestBody](../../models/operations/contacts-update-request-body.md)     | :heavy_check_mark:                                                                                  | N/A                                                                                                 |