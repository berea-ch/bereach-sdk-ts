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

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `account`                                                                                                                                 | [operations.UpdateAccountAccount](../../models/operations/update-account-account.md)                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.UpdateAccountMeta](../../models/operations/update-account-meta.md)                                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |