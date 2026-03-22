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
    proxyConfig: {
      city: null,
      mode: "<value>",
      country: "Guyana",
      rotationHours: 2067.37,
    },
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `account`                                                                            | [operations.UpdateAccountAccount](../../models/operations/update-account-account.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |