# UpsertContactsRequest

## Example Usage

```typescript
import { UpsertContactsRequest } from "bereach/models/operations";

let value: UpsertContactsRequest = {
  contacts: [],
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `contacts`                                                                | [operations.ContactRequest](../../models/operations/contact-request.md)[] | :heavy_check_mark:                                                        | Contacts to add (single or bulk)                                          |