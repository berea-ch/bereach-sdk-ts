# GetFeedMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetFeedMeta } from "bereach/models/operations";

let value: GetFeedMeta = {
  credits: {
    current: 8342.88,
    limit: 2465.89,
    remaining: 2704.55,
    percentage: 9090,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `credits`                                                                | [operations.GetFeedCredits](../../models/operations/get-feed-credits.md) | :heavy_check_mark:                                                       | N/A                                                                      |