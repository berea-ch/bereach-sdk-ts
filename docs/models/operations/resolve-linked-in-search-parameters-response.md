# ResolveLinkedInSearchParametersResponse

Resolved search parameter items

## Example Usage

```typescript
import { ResolveLinkedInSearchParametersResponse } from "bereach/models/operations";

let value: ResolveLinkedInSearchParametersResponse = {
  success: true,
  items: [
    {
      id: "<id>",
      title: "<value>",
      type: "<value>",
    },
  ],
  count: 887158,
  creditsUsed: 970892,
  retryAfter: 960732,
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                               | *true*                                                                                                                  | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `items`                                                                                                                 | [operations.ResolveLinkedInSearchParametersItem](../../models/operations/resolve-linked-in-search-parameters-item.md)[] | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `count`                                                                                                                 | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `creditsUsed`                                                                                                           | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                    |
| `retryAfter`                                                                                                            | *number*                                                                                                                | :heavy_check_mark:                                                                                                      | Seconds to wait before making another call of the same type. 0 means no wait needed.                                    |