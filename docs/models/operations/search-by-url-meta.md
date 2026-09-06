# SearchByUrlMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SearchByUrlMeta } from "bereach/models/operations";

let value: SearchByUrlMeta = {
  credits: {
    current: 7469.92,
    limit: 5133.57,
    remaining: 6733.62,
    percentage: 5421.87,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `credits`                                                                         | [operations.SearchByUrlCredits](../../models/operations/search-by-url-credits.md) | :heavy_check_mark:                                                                | N/A                                                                               |