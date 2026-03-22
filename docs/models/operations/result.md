# Result

## Example Usage

```typescript
import { Result } from "bereach/models/operations";

let value: Result = {
  profile: "<value>",
  status: "pending",
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `profile`                                                           | *string*                                                            | :heavy_check_mark:                                                  | N/A                                                                 |
| `status`                                                            | [operations.ResultStatus](../../models/operations/result-status.md) | :heavy_check_mark:                                                  | N/A                                                                 |
| `contactId`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `error`                                                             | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |