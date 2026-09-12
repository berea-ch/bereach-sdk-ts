# SearchJobsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchJobsMeta } from "bereach/models/operations";

let value: SearchJobsMeta = {
  credits: {
    current: 2173.66,
    limit: 6255.74,
    remaining: 4188.45,
    percentage: 3687.34,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `credits`                                                                      | [operations.SearchJobsCredits](../../models/operations/search-jobs-credits.md) | :heavy_check_mark:                                                             | N/A                                                                            |