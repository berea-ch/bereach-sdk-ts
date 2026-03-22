# SetAgentStateResponse

State saved

## Example Usage

```typescript
import { SetAgentStateResponse } from "bereach/models/operations";

let value: SetAgentStateResponse = {
  success: true,
  key: "<key>",
  data: "<value>",
  updatedAt: "1735606485570",
  creditsUsed: 418934,
  retryAfter: 603925,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `key`                                                                              | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `data`                                                                             | *any*                                                                              | :heavy_check_mark:                                                                 | Full state object                                                                  |
| `updatedAt`                                                                        | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |