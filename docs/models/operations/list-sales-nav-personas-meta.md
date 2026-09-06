# ListSalesNavPersonasMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ListSalesNavPersonasMeta } from "bereach/models/operations";

let value: ListSalesNavPersonasMeta = {
  credits: {
    current: 4573.08,
    limit: 9397.55,
    remaining: 4326.45,
    percentage: 1784.48,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `credits`                                                                                            | [operations.ListSalesNavPersonasCredits](../../models/operations/list-sales-nav-personas-credits.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |