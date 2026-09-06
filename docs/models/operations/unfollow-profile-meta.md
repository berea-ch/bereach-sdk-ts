# UnfollowProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { UnfollowProfileMeta } from "bereach/models/operations";

let value: UnfollowProfileMeta = {
  credits: {
    current: 9322.38,
    limit: null,
    remaining: 9462.22,
    percentage: 3945.96,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.UnfollowProfileCredits](../../models/operations/unfollow-profile-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |