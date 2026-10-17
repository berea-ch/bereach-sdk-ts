# GetProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetProfileMeta } from "bereach/models/operations";

let value: GetProfileMeta = {
  credits: {
    current: 5092.5,
    limit: null,
    remaining: 6557.49,
    percentage: 751.34,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `credits`                                                                      | [operations.GetProfileCredits](../../models/operations/get-profile-credits.md) | :heavy_check_mark:                                                             | N/A                                                                            |