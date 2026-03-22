# GetStatusResponse

Per-profile action completion status

## Example Usage

```typescript
import { GetStatusResponse } from "bereach/models/operations";

let value: GetStatusResponse = {
  success: true,
  profiles: [
    {
      profile: "<value>",
      message: false,
      reply: false,
      like: false,
      visit: true,
      connect: false,
    },
  ],
  creditsUsed: 99528,
  retryAfter: 118952,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `profiles`                                                                         | [operations.GetStatusProfile](../../models/operations/get-status-profile.md)[]     | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for campaign queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for campaign queries). |