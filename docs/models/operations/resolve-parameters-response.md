# ResolveParametersResponse

Resolved search parameter items

## Example Usage

```typescript
import { ResolveParametersResponse } from "bereach/models/operations";

let value: ResolveParametersResponse = {
  success: true,
  items: [
    {
      id: "<id>",
      title: "<value>",
      type: "<value>",
    },
  ],
  count: 763096,
  creditsUsed: 588102,
  retryAfter: 561156,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `success`                                                                                | *true*                                                                                   | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `items`                                                                                  | [operations.ResolveParametersItem](../../models/operations/resolve-parameters-item.md)[] | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `count`                                                                                  | *number*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `creditsUsed`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).     |
| `retryAfter`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Seconds to wait before making another call of the same type. 0 means no wait needed.     |