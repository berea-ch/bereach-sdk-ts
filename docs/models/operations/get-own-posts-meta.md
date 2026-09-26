# GetOwnPostsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetOwnPostsMeta } from "bereach/models/operations";

let value: GetOwnPostsMeta = {
  credits: {
    current: 7213.23,
    limit: 7276.71,
    remaining: 6616.21,
    percentage: 1267.32,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `credits`                                                                         | [operations.GetOwnPostsCredits](../../models/operations/get-own-posts-credits.md) | :heavy_check_mark:                                                                | N/A                                                                               |