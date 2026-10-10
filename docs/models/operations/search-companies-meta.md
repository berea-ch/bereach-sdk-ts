# SearchCompaniesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchCompaniesMeta } from "bereach/models/operations";

let value: SearchCompaniesMeta = {
  credits: {
    current: 8104.43,
    limit: null,
    remaining: null,
    percentage: 9905.91,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.SearchCompaniesCredits](../../models/operations/search-companies-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |