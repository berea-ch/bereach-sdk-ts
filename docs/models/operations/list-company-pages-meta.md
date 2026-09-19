# ListCompanyPagesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListCompanyPagesMeta } from "bereach/models/operations";

let value: ListCompanyPagesMeta = {
  credits: {
    current: 4086.59,
    limit: 916.75,
    remaining: 467.65,
    percentage: 514.57,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `credits`                                                                                   | [operations.ListCompanyPagesCredits](../../models/operations/list-company-pages-credits.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |