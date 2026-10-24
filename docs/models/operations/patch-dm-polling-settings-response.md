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

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `settings`                                                                                                                        | [operations.PatchDmPollingSettingsSettings](../../models/operations/patch-dm-polling-settings-settings.md)                        | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |