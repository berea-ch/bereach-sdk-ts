# ListAccountsResponse

List of LinkedIn accounts

## Example Usage

```typescript
import { ListAccountsResponse } from "bereach/models/operations";

let value: ListAccountsResponse = {
  success: true,
  accounts: [
    {
      id: "<id>",
      label: null,
      isDefault: true,
      isCurrent: false,
      linkedinProfileId: "<id>",
      linkedinName: "<value>",
      linkedinEmail: "<value>",
      profileUrl: "https://snappy-numeric.com/",
      headline: "<value>",
      profilePic: "<value>",
      profileUrn: "<value>",
      isActive: true,
      isValid: false,
      accountPlan: "<value>",
      isUnlimited: true,
      proxyConfig: {
        enabled: false,
      },
      createdAt: "1711331755229",
      updatedAt: "1735680327784",
    },
  ],
  total: 436562,
  isOwner: true,
  creditsUsed: 591899,
  retryAfter: 653111,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `accounts`                                                                                                                                | [operations.ListAccountsAccount](../../models/operations/list-accounts-account.md)[]                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `isOwner`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | True when the caller owns the workspace, in which case `accounts` spans the whole workspace rather than just their own.                   |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ListAccountsMeta](../../models/operations/list-accounts-meta.md)                                                              | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |