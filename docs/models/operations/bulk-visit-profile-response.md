# BulkVisitProfileResponse

Batch accepted and queued for processing

## Example Usage

```typescript
import { BulkVisitProfileResponse } from "bereach/models/operations";

let value: BulkVisitProfileResponse = {
  accepted: true,
  batchId: "<id>",
  profileCount: 854381,
  alreadyCached: 256113,
  willVisit: 408979,
  estimatedMinutes: 4239.95,
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `accepted`                                                  | *true*                                                      | :heavy_check_mark:                                          | N/A                                                         |
| `batchId`                                                   | *string*                                                    | :heavy_check_mark:                                          | Unique batch identifier for status polling.                 |
| `profileCount`                                              | *number*                                                    | :heavy_check_mark:                                          | Total unique profiles in the batch (after dedup).           |
| `alreadyCached`                                             | *number*                                                    | :heavy_check_mark:                                          | Profiles resolved from cache (0 credits, instant).          |
| `willVisit`                                                 | *number*                                                    | :heavy_check_mark:                                          | Profiles queued for LinkedIn API visit.                     |
| `estimatedMinutes`                                          | *number*                                                    | :heavy_check_mark:                                          | Estimated processing time in minutes for uncached profiles. |