# RepostLinkedInPostResponse

Post reposted

## Example Usage

```typescript
import { RepostLinkedInPostResponse } from "bereach/models/operations";

let value: RepostLinkedInPostResponse = {
  success: true,
  shareUrn: "<value>",
  creditsUsed: 408159,
  retryAfter: 5360,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `shareUrn`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |