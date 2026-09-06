# FollowProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { FollowProfileMeta } from "bereach/models/operations";

let value: FollowProfileMeta = {
  credits: {
    current: 2613.35,
    limit: 9660.45,
    remaining: 8842.48,
    percentage: 4339.95,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.FollowProfileCredits](../../models/operations/follow-profile-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |