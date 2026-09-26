# EditProfileMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { EditProfileMeta } from "bereach/models/operations";

let value: EditProfileMeta = {
  credits: {
    current: 4331.04,
    limit: 4146,
    remaining: 5630.01,
    percentage: 1358.41,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `credits`                                                                        | [operations.EditProfileCredits](../../models/operations/edit-profile-credits.md) | :heavy_check_mark:                                                               | N/A                                                                              |