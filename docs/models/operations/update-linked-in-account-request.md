# UpdateLinkedInAccountRequest

## Example Usage

```typescript
import { UpdateLinkedInAccountRequest } from "bereach/models/operations";

let value: UpdateLinkedInAccountRequest = {
  accountId: "<id>",
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `accountId`                                                     | *string*                                                        | :heavy_check_mark:                                              | ID of the LinkedIn account to update.                           |
| `label`                                                         | *string*                                                        | :heavy_minus_sign:                                              | User-facing label (e.g. 'Personal', 'Company SDR').             |
| `isDefault`                                                     | *boolean*                                                       | :heavy_minus_sign:                                              | Set as the default account. Clears default from other accounts. |