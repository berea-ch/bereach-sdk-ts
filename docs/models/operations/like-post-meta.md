# LikePostMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { LikePostMeta } from "bereach/models/operations";

let value: LikePostMeta = {
  credits: {
    current: 1738.04,
    limit: null,
    remaining: 7295.36,
    percentage: 4521.99,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `credits`                                                                  | [operations.LikePostCredits](../../models/operations/like-post-credits.md) | :heavy_check_mark:                                                         | N/A                                                                        |