# ListLinkedInAccountsResponse

List of LinkedIn accounts

## Example Usage

```typescript
import { ListLinkedInAccountsResponse } from "bereach/models/operations";

let value: ListLinkedInAccountsResponse = {
  success: true,
  accounts: [
    {
      id: "<id>",
      label: "<value>",
      isDefault: false,
      isCurrent: true,
      linkedinProfileId: "<id>",
      linkedinName: null,
      linkedinEmail: "<value>",
      profileUrl: "https://grandiose-reboot.net",
      headline: "<value>",
      profilePic: "<value>",
      profileUrn: null,
      isActive: false,
      isValid: true,
      createdAt: "1715398557769",
      updatedAt: "1735670124065",
    },
  ],
  total: 68961,
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `success`                                                                                              | *true*                                                                                                 | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `accounts`                                                                                             | [operations.ListLinkedInAccountsAccount](../../models/operations/list-linked-in-accounts-account.md)[] | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `total`                                                                                                | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |