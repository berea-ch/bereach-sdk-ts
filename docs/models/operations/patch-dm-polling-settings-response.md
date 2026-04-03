# PatchDmPollingSettingsResponse

Settings updated

## Example Usage

```typescript
import { PatchDmPollingSettingsResponse } from "bereach/models/operations";

let value: PatchDmPollingSettingsResponse = {
  success: true,
  settings: {
    dmPollingEnabled: true,
    dmWebhookUrl: "https://partial-draw.org",
    dmLastPolledAt: "<value>",
    connectionPollingEnabled: false,
    connectionLastPolledAt: "<value>",
  },
  creditsUsed: 61139,
  retryAfter: 313727,
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                  | *true*                                                                                                     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `settings`                                                                                                 | [operations.PatchDmPollingSettingsSettings](../../models/operations/patch-dm-polling-settings-settings.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `creditsUsed`                                                                                              | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Credits consumed (always 0 for workspace operations).                                                      |
| `retryAfter`                                                                                               | *number*                                                                                                   | :heavy_check_mark:                                                                                         | Seconds to wait (always 0 for workspace operations).                                                       |