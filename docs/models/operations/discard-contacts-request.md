# DiscardContactsRequest

## Example Usage

```typescript
import { DiscardContactsRequest } from "bereach/models/operations";

let value: DiscardContactsRequest = {
  body: {
    contactIds: [
      "<value 1>",
    ],
    update: {},
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                        | *string*                                                                                            | :heavy_minus_sign:                                                                                  | Scopes the write to one list. Omit it: a chat turn writes to the list of the conversation it is in. |
| `body`                                                                                              | [operations.DiscardContactsRequestBody](../../models/operations/discard-contacts-request-body.md)   | :heavy_check_mark:                                                                                  | N/A                                                                                                 |