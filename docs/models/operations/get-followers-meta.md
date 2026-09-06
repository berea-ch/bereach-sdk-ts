# GetFollowersMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetFollowersMeta } from "bereach/models/operations";

let value: GetFollowersMeta = {
  credits: {
    current: 5527.09,
    limit: 5333.13,
    remaining: 8196.3,
    percentage: 4075.3,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `credits`                                                                          | [operations.GetFollowersCredits](../../models/operations/get-followers-credits.md) | :heavy_check_mark:                                                                 | N/A                                                                                |