# BulkUpdateResponse

Bulk update results

## Example Usage

```typescript
import { BulkUpdateResponse } from "bereach/models/operations";

let value: BulkUpdateResponse = {
  success: true,
  updated: 961120,
  skipped: 546807,
  errors: [],
  creditsUsed: 409666,
  retryAfter: 72240,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `updated`                                                                          | *number*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `skipped`                                                                          | *number*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `errors`                                                                           | *string*[]                                                                         | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |