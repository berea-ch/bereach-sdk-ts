# GetDmPollingSettingsSettings

## Example Usage

```typescript
import { GetDmPollingSettingsSettings } from "bereach/models/operations";

let value: GetDmPollingSettingsSettings = {
  dmPollingEnabled: false,
  dmWebhookUrl: "https://flickering-soup.net",
  dmLastPolledAt: "<value>",
  connectionPollingEnabled: false,
  connectionLastPolledAt: "<value>",
};
```

## Fields

| Field                      | Type                       | Required                   | Description                |
| -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| `dmPollingEnabled`         | *boolean*                  | :heavy_check_mark:         | N/A                        |
| `dmWebhookUrl`             | *string*                   | :heavy_check_mark:         | N/A                        |
| `dmLastPolledAt`           | *string*                   | :heavy_check_mark:         | N/A                        |
| `connectionPollingEnabled` | *boolean*                  | :heavy_check_mark:         | N/A                        |
| `connectionLastPolledAt`   | *string*                   | :heavy_check_mark:         | N/A                        |