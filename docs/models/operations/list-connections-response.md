# ListConnectionsResponse

Connections list

## Example Usage

```typescript
import { ListConnectionsResponse } from "bereach/models/operations";

let value: ListConnectionsResponse = {
  success: true,
  connections: [
    {
      name: "<value>",
      headline: "<value>",
      profileUrl: "https://sure-footed-anticodon.org/",
      imageUrl: "https://fluffy-language.org",
      publicIdentifier: "<value>",
      profileUrn: "<value>",
      connectedAt: "<value>",
    },
  ],
  total: 721340,
  hasMore: false,
  creditsUsed: 106036,
  retryAfter: 549554,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `connections`                                                                        | [operations.Connection](../../models/operations/connection.md)[]                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `hasMore`                                                                            | *boolean*                                                                            | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |