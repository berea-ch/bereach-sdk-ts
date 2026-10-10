# SwitchAccountResponse

Account switched

## Example Usage

```typescript
import { SwitchAccountResponse } from "bereach/models/operations";

let value: SwitchAccountResponse = {
  success: true,
  account: {
    id: "<id>",
    name: "<value>",
    avatar: null,
    plan: "<value>",
  },
  creditsUsed: 900134,
  retryAfter: 243839,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `account`                                                                                                                                 | [operations.SwitchAccountAccount](../../models/operations/switch-account-account.md)                                                      | :heavy_check_mark:                                                                                                                        | Switched account summary                                                                                                                  |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SwitchAccountMeta](../../models/operations/switch-account-meta.md)                                                            | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |