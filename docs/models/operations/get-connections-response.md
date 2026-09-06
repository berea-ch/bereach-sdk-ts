# GetConnectionsResponse

Connections list

## Example Usage

```typescript
import { GetConnectionsResponse } from "bereach/models/operations";

let value: GetConnectionsResponse = {
  success: true,
  connections: [],
  count: 499168,
  start: 779641,
  total: 201594,
  hasMore: true,
  creditsUsed: 945284,
  retryAfter: 770549,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `connections`                                                                                                                             | [operations.Connection](../../models/operations/connection.md)[]                                                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `start`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetConnectionsMeta](../../models/operations/get-connections-meta.md)                                                          | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |