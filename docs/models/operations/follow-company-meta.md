# FollowCompanyMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { FollowCompanyMeta } from "bereach/models/operations";

let value: FollowCompanyMeta = {
  credits: {
    current: 4356.1,
    limit: 6654.21,
    remaining: 6471.35,
    percentage: 6633.22,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.FollowCompanyCredits](../../models/operations/follow-company-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |