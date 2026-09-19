# GetConnectionStatusMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetConnectionStatusMeta } from "bereach/models/operations";

let value: GetConnectionStatusMeta = {
  credits: {
    current: 8651.93,
    limit: 140.36,
    remaining: 2557.66,
    percentage: 7560.82,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `credits`                                                                                         | [operations.GetConnectionStatusCredits](../../models/operations/get-connection-status-credits.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |