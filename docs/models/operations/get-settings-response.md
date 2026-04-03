# GetSettingsResponse

Account settings

## Example Usage

```typescript
import { GetSettingsResponse } from "bereach/models/operations";

let value: GetSettingsResponse = {
  success: true,
  user: {
    id: "<id>",
    name: "<value>",
    email: "Jude22@gmail.com",
    image: "https://picsum.photos/seed/fKf8Mcyb/2321/2366",
    phone: "1-561-396-1017",
    createdAt: "1713759450529",
  },
  location: {
    country: "United States Minor Outlying Islands",
    city: "Champlinworth",
  },
  proxy: {
    enabled: true,
  },
  anthropicKey: {
    isSet: false,
    partial: "<value>",
  },
  subscription: {
    plan: "<value>",
    tier: "<value>",
    proSeatsIncluded: 430854,
    proSeatsUsed: 798187,
    status: "<value>",
    currentPeriodEnd: "<value>",
    hasStripe: false,
  },
  linkedinAccounts: [],
  pendingInvites: [
    {
      id: "<id>",
      email: "Rebeka12@hotmail.com",
      name: "<value>",
      code: "<value>",
      maxUses: 284332,
      useCount: 840312,
      expiresAt: "1747470194361",
      createdAt: "1705635591348",
    },
  ],
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `user`                                                                             | [operations.User](../../models/operations/user.md)                                 | :heavy_check_mark:                                                                 | N/A                                                                                |
| `location`                                                                         | [operations.GetSettingsLocation](../../models/operations/get-settings-location.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `proxy`                                                                            | [operations.Proxy](../../models/operations/proxy.md)                               | :heavy_check_mark:                                                                 | N/A                                                                                |
| `anthropicKey`                                                                     | [operations.AnthropicKey](../../models/operations/anthropic-key.md)                | :heavy_check_mark:                                                                 | N/A                                                                                |
| `subscription`                                                                     | [operations.Subscription](../../models/operations/subscription.md)                 | :heavy_check_mark:                                                                 | N/A                                                                                |
| `linkedinAccounts`                                                                 | [operations.LinkedinAccount](../../models/operations/linkedin-account.md)[]        | :heavy_check_mark:                                                                 | N/A                                                                                |
| `pendingInvites`                                                                   | [operations.PendingInvite](../../models/operations/pending-invite.md)[]            | :heavy_check_mark:                                                                 | N/A                                                                                |