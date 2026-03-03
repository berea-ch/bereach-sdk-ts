# ResolveLinkedInSearchParametersResponse

Resolved search parameter items

## Example Usage

```typescript
import { ResolveLinkedInSearchParametersResponse } from "bereach/models/operations";

let value: ResolveLinkedInSearchParametersResponse = {
  success: false,
  items: [
    {
      id: "<id>",
      title: "<value>",
      type: "<value>",
    },
  ],
  count: 970892,
  creditsUsed: 960732,
  retryAfter: 104643,
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                               | *boolean*                                                                                                               | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `items`                                                                                                                 | [operations.ResolveLinkedInSearchParametersItem](../../models/operations/resolve-linked-in-search-parameters-item.md)[] | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `count`                                                                                                                 | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `creditsUsed`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                    |
| `retryAfter`                                                                                                            | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Seconds to wait before making another call of the same type. 0 means no wait needed.                                    |