# GetDmPollingSettingsMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { GetDmPollingSettingsMeta } from "bereach/models/operations";

let value: GetDmPollingSettingsMeta = {
  credits: {
    current: 567.81,
    limit: 7569.77,
    remaining: 6989.97,
    percentage: 4407.96,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `credits`                                                                                            | [operations.GetDmPollingSettingsCredits](../../models/operations/get-dm-polling-settings-credits.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |