# RevalidateLinkedinResponse

Validation result

## Example Usage

```typescript
import { RevalidateLinkedinResponse } from "bereach/models/operations";

let value: RevalidateLinkedinResponse = {
  success: true,
  message: "<value>",
  wasInvalid: false,
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `success`                                          | *true*                                             | :heavy_check_mark:                                 | N/A                                                |
| `message`                                          | *string*                                           | :heavy_check_mark:                                 | N/A                                                |
| `wasInvalid`                                       | *boolean*                                          | :heavy_check_mark:                                 | True if credentials were previously marked invalid |