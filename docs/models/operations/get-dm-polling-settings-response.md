# GetDmPollingSettingsResponse

Polling settings

## Example Usage

```typescript
import { GetDmPollingSettingsResponse } from "bereach/models/operations";

let value: GetDmPollingSettingsResponse = {
  success: true,
  settings: {
    dmWebhookUrl: "https://stunning-importance.org/",
    connectionLastPolledAt: "<value>",
  },
  creditsUsed: 26670,
  retryAfter: 743559,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `settings`                                                                                                                                | [operations.GetDmPollingSettingsSettings](../../models/operations/get-dm-polling-settings-settings.md)                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetDmPollingSettingsMeta](../../models/operations/get-dm-polling-settings-meta.md)                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |