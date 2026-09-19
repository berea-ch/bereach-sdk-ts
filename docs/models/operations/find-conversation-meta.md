# FindConversationMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { FindConversationMeta } from "bereach/models/operations";

let value: FindConversationMeta = {
  credits: {
    current: 7970.51,
    limit: 3077.48,
    remaining: 5756.84,
    percentage: 7787.49,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `credits`                                                                                  | [operations.FindConversationCredits](../../models/operations/find-conversation-credits.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |