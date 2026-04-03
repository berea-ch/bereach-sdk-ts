# GetDmPollingSettingsResponse

Polling settings

## Example Usage

```typescript
import { GetDmPollingSettingsResponse } from "bereach/models/operations";

let value: GetDmPollingSettingsResponse = {
  success: true,
  settings: {
    dmPollingEnabled: true,
    dmWebhookUrl: null,
    dmLastPolledAt: "<value>",
    connectionPollingEnabled: true,
    connectionLastPolledAt: "<value>",
  },
  creditsUsed: 910875,
  retryAfter: 26670,
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `success`                                                                                              | *true*                                                                                                 | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `settings`                                                                                             | [operations.GetDmPollingSettingsSettings](../../models/operations/get-dm-polling-settings-settings.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `creditsUsed`                                                                                          | *number*                                                                                               | :heavy_check_mark:                                                                                     | Credits consumed (always 0 for workspace operations).                                                  |
| `retryAfter`                                                                                           | *number*                                                                                               | :heavy_check_mark:                                                                                     | Seconds to wait (always 0 for workspace operations).                                                   |