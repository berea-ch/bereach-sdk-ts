# VisitProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { VisitProfileMeta } from "bereach/models/operations";

let value: VisitProfileMeta = {
  credits: {
    current: 4893.49,
    limit: 4793.87,
    remaining: 2182.69,
    percentage: 5521.41,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.VisitProfileCredits](../../models/operations/visit-profile-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |