# PublicEnrichRequest

## Example Usage

```typescript
import { PublicEnrichRequest } from "bereach/models/operations";

let value: PublicEnrichRequest = {
  contactIds: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `contactIds`                                                                                                   | *string*[]                                                                                                     | :heavy_check_mark:                                                                                             | Which of your own contacts to (re)fetch. An explicit list — not a filter — so nothing is enriched by accident. |
| `campaignId`                                                                                                   | *string*                                                                                                       | :heavy_minus_sign:                                                                                             | Link newly-touched contacts to this list (slug or id). In chat, omit it: the conversation's own list is used.  |
| `qualify`                                                                                                      | *boolean*                                                                                                      | :heavy_minus_sign:                                                                                             | Also grade the enriched contacts against the list's ICP, off unless the grading was asked for.                 |