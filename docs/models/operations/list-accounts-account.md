# ListAccountsAccount

## Example Usage

```typescript
import { ListAccountsAccount } from "bereach/models/operations";

let value: ListAccountsAccount = {
  id: "<id>",
  label: "<value>",
  isDefault: true,
  isCurrent: false,
  linkedinProfileId: "<id>",
  linkedinName: null,
  linkedinEmail: null,
  profileUrl: "https://submissive-sailor.net/",
  headline: "<value>",
  profilePic: "<value>",
  profileUrn: "<value>",
  isActive: false,
  isValid: true,
  accountPlan: "<value>",
  isUnlimited: true,
  creditsLimit: 725893,
  creditsCount: 729705,
  proxyConfig: {
    enabled: false,
  },
  createdAt: "1712114071971",
  updatedAt: "1735674717366",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `label`                                                                                     | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isDefault`                                                                                 | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isCurrent`                                                                                 | *boolean*                                                                                   | :heavy_check_mark:                                                                          | Whether this account is the one used by the current API token.                              |
| `linkedinProfileId`                                                                         | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `linkedinName`                                                                              | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `linkedinEmail`                                                                             | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `profileUrl`                                                                                | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `headline`                                                                                  | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `profilePic`                                                                                | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `profileUrn`                                                                                | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isActive`                                                                                  | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isValid`                                                                                   | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `accountPlan`                                                                               | *string*                                                                                    | :heavy_check_mark:                                                                          | Account plan tier (e.g. 'free', 'pro', 'team').                                             |
| `isUnlimited`                                                                               | *boolean*                                                                                   | :heavy_check_mark:                                                                          | Whether this account has unlimited credits.                                                 |
| `creditsLimit`                                                                              | *number*                                                                                    | :heavy_check_mark:                                                                          | Monthly credit limit for this account. Null if unlimited.                                   |
| `creditsCount`                                                                              | *number*                                                                                    | :heavy_check_mark:                                                                          | Credits used in the current billing period.                                                 |
| `proxyConfig`                                                                               | [operations.ListAccountsProxyConfig](../../models/operations/list-accounts-proxy-config.md) | :heavy_check_mark:                                                                          | Proxy status for this account. Full config is masked; only enabled flag is exposed.         |
| `createdAt`                                                                                 | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `updatedAt`                                                                                 | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |