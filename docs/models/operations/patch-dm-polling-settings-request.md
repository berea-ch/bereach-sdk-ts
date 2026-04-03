# PatchDmPollingSettingsRequest

## Example Usage

```typescript
import { PatchDmPollingSettingsRequest } from "bereach/models/operations";

let value: PatchDmPollingSettingsRequest = {};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `dmPollingEnabled`                            | *boolean*                                     | :heavy_minus_sign:                            | N/A                                           |
| `dmWebhookUrl`                                | *string*                                      | :heavy_minus_sign:                            | Webhook URL for DM events                     |
| `connectionPollingEnabled`                    | *boolean*                                     | :heavy_minus_sign:                            | Enable polling to detect accepted connections |