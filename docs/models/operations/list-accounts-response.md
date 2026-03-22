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
      creditsLimit: 227618,
      creditsCount: 892693,
      proxyConfig: {
        enabled: false,
      },
      createdAt: "1718165763136",
      updatedAt: "1735654339471",
    },
  ],
  total: 653111,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `accounts`                                                                           | [operations.ListAccountsAccount](../../models/operations/list-accounts-account.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |