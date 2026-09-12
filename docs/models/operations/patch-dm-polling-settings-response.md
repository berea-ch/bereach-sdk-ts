# PatchDmPollingSettingsResponse

Settings updated

## Example Usage

```typescript
import { PatchDmPollingSettingsResponse } from "bereach/models/operations";

let value: PatchDmPollingSettingsResponse = {
  success: true,
  settings: {
    dmWebhookUrl: "https://rotating-necklace.biz",
    connectionLastPolledAt: "<value>",
  },
  creditsUsed: 335675,
  retryAfter: 768553,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `settings`                                                                                                                                | [operations.PatchDmPollingSettingsSettings](../../models/operations/patch-dm-polling-settings-settings.md)                                | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.PatchDmPollingSettingsMeta](../../models/operations/patch-dm-polling-settings-meta.md)                                        | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |