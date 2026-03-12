# UpdateLinkedInAccountResponse

Updated account

## Example Usage

```typescript
import { UpdateLinkedInAccountResponse } from "bereach/models/operations";

let value: UpdateLinkedInAccountResponse = {
  success: true,
  account: {
    id: "<id>",
    label: "<value>",
    isDefault: false,
    linkedinProfileId: "<id>",
    linkedinName: "<value>",
    headline: "<value>",
    profilePic: "<value>",
    isValid: true,
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `success`                                                                                              | *true*                                                                                                 | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `account`                                                                                              | [operations.UpdateLinkedInAccountAccount](../../models/operations/update-linked-in-account-account.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |