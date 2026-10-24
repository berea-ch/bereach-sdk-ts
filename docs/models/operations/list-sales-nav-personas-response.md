# ListSalesNavPersonasResponse

User's saved personas.

## Example Usage

```typescript
import { ListSalesNavPersonasResponse } from "bereach/models/operations";

let value: ListSalesNavPersonasResponse = {
  success: true,
  personas: [],
  count: 363851,
  creditsUsed: 120172,
  retryAfter: 630741,
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                         | *true*                                                                                                                            | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `personas`                                                                                                                        | [operations.Persona](../../models/operations/persona.md)[]                                                                        | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `count`                                                                                                                           | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | N/A                                                                                                                               |
| `creditsUsed`                                                                                                                     | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Credits this call spent, net of anything given back. 0 when nothing was charged: a free read, a cached answer, nothing delivered. |
| `retryAfter`                                                                                                                      | *number*                                                                                                                          | :heavy_check_mark:                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                  |