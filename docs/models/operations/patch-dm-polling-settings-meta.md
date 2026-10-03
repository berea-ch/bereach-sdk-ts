# PatchDmPollingSettingsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { PatchDmPollingSettingsMeta } from "bereach/models/operations";

let value: PatchDmPollingSettingsMeta = {
  credits: {
    current: 6814.33,
    limit: 7686.53,
    remaining: 8992.35,
    percentage: 5480.71,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `credits`                                                                                                | [operations.PatchDmPollingSettingsCredits](../../models/operations/patch-dm-polling-settings-credits.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |