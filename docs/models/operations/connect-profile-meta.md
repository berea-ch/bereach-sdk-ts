# ConnectProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ConnectProfileMeta } from "bereach/models/operations";

let value: ConnectProfileMeta = {
  credits: {
    current: 1530.38,
    limit: 294.42,
    remaining: 9680.22,
    percentage: 7957.31,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | [operations.ConnectProfileCredits](../../models/operations/connect-profile-credits.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |