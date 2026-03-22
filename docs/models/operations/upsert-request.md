# UpsertRequest

## Example Usage

```typescript
import { UpsertRequest } from "bereach/models/operations";

let value: UpsertRequest = {
  contacts: [],
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `contacts`                                                                             | [operations.UpsertContactRequest](../../models/operations/upsert-contact-request.md)[] | :heavy_check_mark:                                                                     | Contacts to add (single or bulk)                                                       |