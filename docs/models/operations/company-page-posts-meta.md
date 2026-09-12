# CompanyPagePostsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CompanyPagePostsMeta } from "bereach/models/operations";

let value: CompanyPagePostsMeta = {
  credits: {
    current: 738.84,
    limit: 8451.07,
    remaining: 1881.03,
    percentage: 4023.46,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `credits`                                                                                   | [operations.CompanyPagePostsCredits](../../models/operations/company-page-posts-credits.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |