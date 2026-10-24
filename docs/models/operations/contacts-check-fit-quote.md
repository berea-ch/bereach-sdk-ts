# ContactsCheckFitQuote

## Example Usage

```typescript
import { ContactsCheckFitQuote } from "bereach/models/operations";

let value: ContactsCheckFitQuote = {
  kind: "fit",
  people: 87362,
  alreadyDone: 347288,
  credits: 6622.72,
  creditsLeft: 3654.05,
  confirm: true,
  affordable: true,
  affordablePeople: 64784,
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `kind`                                                                                           | [operations.ContactsCheckFitQuoteKind](../../models/operations/contacts-check-fit-quote-kind.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `people`                                                                                         | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `alreadyDone`                                                                                    | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `credits`                                                                                        | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `creditsLeft`                                                                                    | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `confirm`                                                                                        | *boolean*                                                                                        | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `affordable`                                                                                     | *boolean*                                                                                        | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `affordablePeople`                                                                               | *number*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `extra`                                                                                          | Record<string, *number*>                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |