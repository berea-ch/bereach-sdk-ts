# UpdateAccountResponse

Updated account

## Example Usage

```typescript
import { UpdateAccountResponse } from "bereach/models/operations";

let value: UpdateAccountResponse = {
  success: true,
  account: {
    id: "<id>",
    label: "<value>",
    isDefault: true,
    linkedinProfileId: "<id>",
    linkedinName: "<value>",
    headline: "<value>",
    profilePic: "<value>",
    isValid: true,
    isActive: true,
    proxyConfig: {
      city: "Clifton",
      mode: "<value>",
      country: "Sint Maarten",
      rotationHours: 4302.5,
    },
  },
  creditsUsed: 82554,
  retryAfter: 763060,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `account`                                                                                                                         | [operations.UpdateAccountAccount](../../models/operations/update-account-account.md)                                              | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |