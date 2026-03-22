# PatchAgentStateResponse

State merged

## Example Usage

```typescript
import { PatchAgentStateResponse } from "bereach/models/operations";

let value: PatchAgentStateResponse = {
  success: true,
  key: "<key>",
  data: "<value>",
  updatedAt: "1735663828921",
  creditsUsed: 67465,
  retryAfter: 701008,
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