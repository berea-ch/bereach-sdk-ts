# BulkVisitBatchStatusResponse

Batch status

## Example Usage

```typescript
import { BulkVisitBatchStatusResponse } from "bereach/models/operations";

let value: BulkVisitBatchStatusResponse = {
  batchId: "<id>",
  status: "failed",
  progress: {
    total: 982849,
    visited: 366923,
    cached: 332902,
    failed: 511229,
    skipped: 758655,
    pending: 403259,
  },
  creditsUsed: 848125,
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `batchId`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `status`                                                                                           | [operations.BulkVisitBatchStatusStatus](../../models/operations/bulk-visit-batch-status-status.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `progress`                                                                                         | [operations.Progress](../../models/operations/progress.md)                                         | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `creditsUsed`                                                                                      | *number*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `failureReason`                                                                                    | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `results`                                                                                          | [operations.Result](../../models/operations/result.md)[]                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |