# InboxUnreadCountMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { InboxUnreadCountMeta } from "bereach/models/operations";

let value: InboxUnreadCountMeta = {
  credits: {
    current: 4773.62,
    limit: 8874.29,
    remaining: 4689.1,
    percentage: 865.17,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `credits`                                                                                   | [operations.InboxUnreadCountCredits](../../models/operations/inbox-unread-count-credits.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |