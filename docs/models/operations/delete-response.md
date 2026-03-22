# DeleteResponse

Context deleted

## Example Usage

```typescript
import { DeleteResponse } from "bereach/models/operations";

let value: DeleteResponse = {
  success: true,
  creditsUsed: 933250,
  retryAfter: 316100,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `success`                                             | *true*                                                | :heavy_check_mark:                                    | N/A                                                   |
| `creditsUsed`                                         | *number*                                              | :heavy_check_mark:                                    | Credits consumed (always 0 for workspace operations). |
| `retryAfter`                                          | *number*                                              | :heavy_check_mark:                                    | Seconds to wait (always 0 for workspace operations).  |