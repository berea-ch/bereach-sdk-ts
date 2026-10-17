# SendMessageMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { SendMessageMeta } from "bereach/models/operations";

let value: SendMessageMeta = {
  credits: {
    current: 3991.66,
    limit: 7873.78,
    remaining: 4642.18,
    percentage: 3281.68,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.SendMessageCredits](../../models/operations/send-message-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |