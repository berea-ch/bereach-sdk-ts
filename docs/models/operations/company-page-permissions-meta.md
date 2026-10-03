# CompanyPagePermissionsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CompanyPagePermissionsMeta } from "bereach/models/operations";

let value: CompanyPagePermissionsMeta = {
  credits: {
    current: 6110.35,
    limit: 3979.62,
    remaining: 8770.27,
    percentage: 1391.19,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.CompanyPagePermissionsCredits](../../models/operations/company-page-permissions-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |