# Needs

A quote, not an answer: this ask carries facets only the connected account can honour, and nothing was run or spent. Relay it plainly, ask the user, and repeat the call with approveLinkedInSpend true only after they agree. contacts is empty alongside this by construction.

## Example Usage

```typescript
import { Needs } from "bereach/models/operations";

let value: Needs = {
  kind: "linkedin_spend",
  because: [
    {
      field: "<value>",
      value: "<value>",
    },
  ],
  estimate: {
    linkedinSearches: 415434,
  },
  alternative: "<value>",
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `kind`                                                                                | [operations.PublicFindPeopleKind](../../models/operations/public-find-people-kind.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `because`                                                                             | [operations.Because](../../models/operations/because.md)[]                            | :heavy_check_mark:                                                                    | The facets that need the connected account.                                           |
| `estimate`                                                                            | [operations.Estimate](../../models/operations/estimate.md)                            | :heavy_check_mark:                                                                    | What approving would spend, in LinkedIn searches.                                     |
| `alternative`                                                                         | *string*                                                                              | :heavy_check_mark:                                                                    | The no-spend path, ready to relay.                                                    |