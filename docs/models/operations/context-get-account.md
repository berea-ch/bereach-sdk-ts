# ContextGetAccount

## Example Usage

```typescript
import { ContextGetAccount } from "bereach/models/operations";

let value: ContextGetAccount = {
  id: "<id>",
  name: "<value>",
  plan: "<value>",
  headline: "<value>",
  status: "expired",
  isUnlimited: false,
  creditsLimit: 731691,
  creditsCount: 497786,
  simulateWrites: true,
  isCurrent: false,
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `name`                                                                                      | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `plan`                                                                                      | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `headline`                                                                                  | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `status`                                                                                    | [operations.ContextGetAccountStatus](../../models/operations/context-get-account-status.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isUnlimited`                                                                               | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `creditsLimit`                                                                              | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `creditsCount`                                                                              | *number*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `simulateWrites`                                                                            | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `isCurrent`                                                                                 | *boolean*                                                                                   | :heavy_check_mark:                                                                          | N/A                                                                                         |