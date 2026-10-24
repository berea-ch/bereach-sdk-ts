# ContactsAddSignalsQuote

## Example Usage

```typescript
import { ContactsAddSignalsQuote } from "bereach/models/operations";

let value: ContactsAddSignalsQuote = {
  kind: "email",
  people: 908178,
  alreadyDone: 602784,
  credits: 8165.65,
  creditsLeft: 3094.94,
  confirm: true,
  affordable: false,
  affordablePeople: 239882,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `kind`                                                                                               | [operations.ContactsAddSignalsQuoteKind](../../models/operations/contacts-add-signals-quote-kind.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `people`                                                                                             | *number*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `alreadyDone`                                                                                        | *number*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `credits`                                                                                            | *number*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `creditsLeft`                                                                                        | *number*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `confirm`                                                                                            | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `affordable`                                                                                         | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `affordablePeople`                                                                                   | *number*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `extra`                                                                                              | Record<string, *number*>                                                                             | :heavy_minus_sign:                                                                                   | N/A                                                                                                  |