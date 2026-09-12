# InboxListMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { InboxListMeta } from "bereach/models/operations";

let value: InboxListMeta = {
  credits: {
    current: 7940.7,
    limit: 7115.76,
    remaining: null,
    percentage: 5273.33,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `credits`                                                                    | [operations.InboxListCredits](../../models/operations/inbox-list-credits.md) | :heavy_check_mark:                                                           | N/A                                                                          |