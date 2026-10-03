# UnfollowCompanyMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UnfollowCompanyMeta } from "bereach/models/operations";

let value: UnfollowCompanyMeta = {
  credits: {
    current: 4669.06,
    limit: null,
    remaining: 7614.78,
    percentage: 9722.18,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.UnfollowCompanyCredits](../../models/operations/unfollow-company-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |