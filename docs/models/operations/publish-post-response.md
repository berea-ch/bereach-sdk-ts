# PublishPostResponse

Post published or scheduled successfully

## Example Usage

```typescript
import { PublishPostResponse } from "bereach/models/operations";

let value: PublishPostResponse = {
  success: true,
  shareUrn: "<value>",
  activityUrn: "<value>",
  creditsUsed: 861088,
  retryAfter: 414220,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `shareUrn`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | URN of the created share (e.g., 'urn:li:fsd_share:urn:li:share:123...')              |
| `activityUrn`                                                                        | *string*                                                                             | :heavy_check_mark:                                                                   | Activity URN (only available for instant mode)                                       |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | True if this action was already executed for the given campaignSlug + target.        |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |