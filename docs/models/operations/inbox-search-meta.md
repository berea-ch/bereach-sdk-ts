# InboxSearchMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { InboxSearchMeta } from "bereach/models/operations";

let value: InboxSearchMeta = {
  credits: {
    current: 8492.37,
    limit: 1782.17,
    remaining: 6205.79,
    percentage: 344.08,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.InboxSearchCredits](../../models/operations/inbox-search-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |