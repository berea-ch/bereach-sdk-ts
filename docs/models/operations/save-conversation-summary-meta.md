# SaveConversationSummaryMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SaveConversationSummaryMeta } from "bereach/models/operations";

let value: SaveConversationSummaryMeta = {
  credits: {
    current: 9055.6,
    limit: 8739.24,
    remaining: 3707.01,
    percentage: 4192.28,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                                 | [operations.SaveConversationSummaryCredits](../../models/operations/save-conversation-summary-credits.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |