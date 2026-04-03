# LinkedinAccount

## Example Usage

```typescript
import { LinkedinAccount } from "bereach/models/operations";

let value: LinkedinAccount = {
  id: "<id>",
  label: "<value>",
  isDefault: true,
  linkedinName: "<value>",
  linkedinEmail: "<value>",
  profilePic: "<value>",
  profileUrl: "https://cool-outrun.name",
  headline: "<value>",
  isValid: false,
  isActive: true,
  validationError: "<value>",
  accountPlan: "<value>",
  credits: {
    current: 183280,
    limit: null,
    isUnlimited: false,
  },
  proxy: {
    enabled: false,
  },
  apiKey: {
    partialKey: "<value>",
    createdAt: "1713408879245",
  },
  createdAt: "1723494551666",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `label`                                                                              | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `isDefault`                                                                          | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `linkedinName`                                                                       | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `linkedinEmail`                                                                      | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `profilePic`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `profileUrl`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `headline`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `isValid`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `isActive`                                                                           | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `validationError`                                                                    | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `accountPlan`                                                                        | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `credits`                                                                            | [operations.GetSettingsCredits](../../models/operations/get-settings-credits.md)     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `proxy`                                                                              | [operations.LinkedinAccountProxy](../../models/operations/linkedin-account-proxy.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `apiKey`                                                                             | [operations.ApiKey](../../models/operations/api-key.md)                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `createdAt`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |