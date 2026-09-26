# SearchEmployeesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchEmployeesMeta } from "bereach/models/operations";

let value: SearchEmployeesMeta = {
  credits: {
    current: 2014.09,
    limit: 2467.68,
    remaining: null,
    percentage: 6194.01,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.SearchEmployeesCredits](../../models/operations/search-employees-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |