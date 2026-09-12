# GetConversationSummaryMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetConversationSummaryMeta } from "bereach/models/operations";

let value: GetConversationSummaryMeta = {
  credits: {
    current: 2717.72,
    limit: 7022.51,
    remaining: 4422.3,
    percentage: 155.22,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                               | [operations.GetConversationSummaryCredits](../../models/operations/get-conversation-summary-credits.md) | :heavy_check_mark:                                                                                      | N/A                                                                                                     |