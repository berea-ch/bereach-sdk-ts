# ResponseBodyNotFoundError1

## Example Usage

```typescript
import { ResponseBodyNotFoundError1 } from "bereach/models/errors";

// No examples available for this model
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `success`                                             | *false*                                               | :heavy_minus_sign:                                    | N/A                                                   |
| `error`                                               | *string*                                              | :heavy_check_mark:                                    | What went wrong, in words.                            |
| `code`                                                | *string*                                              | :heavy_minus_sign:                                    | A machine-readable code, when the answer carries one. |
| `message`                                             | *string*                                              | :heavy_minus_sign:                                    | N/A                                                   |
| `target`                                              | *string*                                              | :heavy_minus_sign:                                    | The address the failure was about, when there is one. |
| `retryAfter`                                          | *number*                                              | :heavy_minus_sign:                                    | Seconds to wait before retrying.                      |
| `upgradeUrl`                                          | *string*                                              | :heavy_minus_sign:                                    | N/A                                                   |