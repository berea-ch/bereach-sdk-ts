# GetLinkedInSearchAppearancesResponse

Search appearance stats

## Example Usage

```typescript
import { GetLinkedInSearchAppearancesResponse } from "bereach/models/operations";

let value: GetLinkedInSearchAppearancesResponse = {
  success: true,
  appearances: "<value>",
  creditsUsed: 296879,
  retryAfter: 978144,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `appearances`                                                                        | *any*                                                                                | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |