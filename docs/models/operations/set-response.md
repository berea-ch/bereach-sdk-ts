# SetResponse

Context saved

## Example Usage

```typescript
import { SetResponse } from "bereach/models/operations";

let value: SetResponse = {
  success: true,
  entry: {
    type: "<value>",
    label: "<value>",
    content: "<value>",
    scope: "<value>",
    updatedAt: "1735605158354",
  },
  creditsUsed: 102892,
  retryAfter: 488152,
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `success`                                                   | *true*                                                      | :heavy_check_mark:                                          | N/A                                                         |
| `entry`                                                     | [operations.SetEntry](../../models/operations/set-entry.md) | :heavy_check_mark:                                          | N/A                                                         |
| `creditsUsed`                                               | *number*                                                    | :heavy_check_mark:                                          | Credits consumed (always 0 for workspace operations).       |
| `retryAfter`                                                | *number*                                                    | :heavy_check_mark:                                          | Seconds to wait (always 0 for workspace operations).        |