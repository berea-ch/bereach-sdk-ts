# SearchPeopleMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchPeopleMeta } from "bereach/models/operations";

let value: SearchPeopleMeta = {
  credits: {
    current: 4037.83,
    limit: 7905.21,
    remaining: 4098.6,
    percentage: 794.75,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.SearchPeopleCredits](../../models/operations/search-people-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |