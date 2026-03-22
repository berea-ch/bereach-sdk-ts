# GetSearchAppearancesResponse

Search appearance stats

## Example Usage

```typescript
import { GetSearchAppearancesResponse } from "bereach/models/operations";

let value: GetSearchAppearancesResponse = {
  success: true,
  appearances: {
    count: 319234,
    keywords: [
      "<value 1>",
    ],
    companies: [
      "<value 1>",
      "<value 2>",
    ],
    raw: "<value>",
  },
  creditsUsed: 620670,
  retryAfter: 51609,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `appearances`                                                                        | [operations.Appearances](../../models/operations/appearances.md)                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |