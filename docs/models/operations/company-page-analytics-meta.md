# CompanyPageAnalyticsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { CompanyPageAnalyticsMeta } from "bereach/models/operations";

let value: CompanyPageAnalyticsMeta = {
  credits: {
    current: 4699.93,
    limit: 5406.44,
    remaining: 8335.91,
    percentage: 547.37,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `credits`                                                                                           | [operations.CompanyPageAnalyticsCredits](../../models/operations/company-page-analytics-credits.md) | :heavy_check_mark:                                                                                  | N/A                                                                                                 |