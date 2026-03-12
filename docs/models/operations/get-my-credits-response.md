# GetMyCreditsResponse

Credit balance for the workspace

## Example Usage

```typescript
import { GetMyCreditsResponse } from "bereach/models/operations";

let value: GetMyCreditsResponse = {
  success: true,
  credits: {
    current: 276462,
    limit: 81044,
    remaining: 613462,
    percentage: 6748.51,
  },
  creditsUsed: 103424,
  retryAfter: 595654,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `credits`                                                                            | [operations.Credits](../../models/operations/credits.md)                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |