# GetRecommendedPeopleMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetRecommendedPeopleMeta } from "bereach/models/operations";

let value: GetRecommendedPeopleMeta = {
  credits: {
    current: 4456.06,
    limit: 1572.43,
    remaining: null,
    percentage: 4964.9,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `credits`                                                                                           | [operations.GetRecommendedPeopleCredits](../../models/operations/get-recommended-people-credits.md) | :heavy_check_mark:                                                                                  | N/A                                                                                                 |