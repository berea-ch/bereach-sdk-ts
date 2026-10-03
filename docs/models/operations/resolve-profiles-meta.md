# ResolveProfilesMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { ResolveProfilesMeta } from "bereach/models/operations";

let value: ResolveProfilesMeta = {
  credits: {
    current: 7116.09,
    limit: 2831.44,
    remaining: 1587.87,
    percentage: 3689.78,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `credits`                                                                                | [operations.ResolveProfilesCredits](../../models/operations/resolve-profiles-credits.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |