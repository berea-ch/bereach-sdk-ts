# GetConnectionsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetConnectionsMeta } from "bereach/models/operations";

let value: GetConnectionsMeta = {
  credits: {
    current: 8868.72,
    limit: 4800.71,
    remaining: 9862.29,
    percentage: 6900.27,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `credits`                                                                              | [operations.GetConnectionsCredits](../../models/operations/get-connections-credits.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |