# SearchSalesNavPeopleMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchSalesNavPeopleMeta } from "bereach/models/operations";

let value: SearchSalesNavPeopleMeta = {
  credits: {
    current: 205.45,
    limit: 9348.7,
    remaining: 1704.36,
    percentage: 1883.15,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `credits`                                                                                            | [operations.SearchSalesNavPeopleCredits](../../models/operations/search-sales-nav-people-credits.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |