# ResolveLinkedInSearchParametersTooManyRequestsError

## Example Usage

```typescript
import { ResolveLinkedInSearchParametersTooManyRequestsError } from "bereach/models/operations";

let value: ResolveLinkedInSearchParametersTooManyRequestsError = {
  code: "rate_limit_exceeded",
  message: "<value>",
  retryAfter: 520259,
  daily: {
    current: 771197,
    limit: 239786,
  },
  weekly: {
    current: 511862,
    limit: 103453,
  },
};
```

## Fields

| Field                                                                                                                     | Type                                                                                                                      | Required                                                                                                                  | Description                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                                    | [operations.ResolveLinkedInSearchParametersCode](../../models/operations/resolve-linked-in-search-parameters-code.md)     | :heavy_check_mark:                                                                                                        | N/A                                                                                                                       |
| `message`                                                                                                                 | *string*                                                                                                                  | :heavy_check_mark:                                                                                                        | N/A                                                                                                                       |
| `docs`                                                                                                                    | *string*                                                                                                                  | :heavy_minus_sign:                                                                                                        | N/A                                                                                                                       |
| `retryAfter`                                                                                                              | *number*                                                                                                                  | :heavy_check_mark:                                                                                                        | Seconds to wait before retrying.                                                                                          |
| `daily`                                                                                                                   | [operations.ResolveLinkedInSearchParametersDaily](../../models/operations/resolve-linked-in-search-parameters-daily.md)   | :heavy_check_mark:                                                                                                        | Current and max daily usage (null if no daily cap).                                                                       |
| `weekly`                                                                                                                  | [operations.ResolveLinkedInSearchParametersWeekly](../../models/operations/resolve-linked-in-search-parameters-weekly.md) | :heavy_check_mark:                                                                                                        | Current and max weekly usage (null if no weekly cap).                                                                     |