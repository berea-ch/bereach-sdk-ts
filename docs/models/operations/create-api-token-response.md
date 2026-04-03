# CreateApiTokenResponse

Token created

## Example Usage

```typescript
import { CreateApiTokenResponse } from "bereach/models/operations";

let value: CreateApiTokenResponse = {
  success: true,
  token: "<value>",
  partialKey: "<value>",
  accountId: "<id>",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `success`                                  | *true*                                     | :heavy_check_mark:                         | N/A                                        |
| `token`                                    | *string*                                   | :heavy_check_mark:                         | Full API token (brc_...) - only shown once |
| `partialKey`                               | *string*                                   | :heavy_check_mark:                         | N/A                                        |
| `accountId`                                | *string*                                   | :heavy_check_mark:                         | N/A                                        |