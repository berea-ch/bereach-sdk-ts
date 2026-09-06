# GetConnectionStatusResponse

Current state of the connection-request lane

## Example Usage

```typescript
import { GetConnectionStatusResponse } from "bereach/models/operations";

let value: GetConnectionStatusResponse = {
  success: true,
  accounts: [],
  totals: {
    waitingTotal: 152562,
    awaitingResponse: 606106,
    sentLast24h: 180372,
    acceptedLast24h: 672000,
    expectedNext24h: 783378,
    expectedIsPartial: true,
    oldestWaitingHours: 560369,
    accountsSending: 208135,
    accountsBlocked: 46185,
    accountsUnreadable: 968776,
    next: {
      contactId: "<id>",
      name: "<value>",
      avatarUrl: "https://dependable-widow.name/",
      headline: "<value>",
      linkedinUrl: "https://calculating-outrun.com",
      lastActivityAt: "<value>",
      thinProfile: false,
      why: {
        status: "waiting",
        detail: "<value>",
        clearsItself: true,
        fixUrl: "https://heavy-eggplant.net/",
      },
      position: 700719,
      etaDays: 6396.43,
      accountLabel: "<value>",
    },
  },
  creditsUsed: 124958,
  retryAfter: 837493,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `accounts`                                                                                                                                | [operations.GetConnectionStatusAccount](../../models/operations/get-connection-status-account.md)[]                                       | :heavy_check_mark:                                                                                                                        | One entry per connected LinkedIn account. Accounts send independently and in parallel, each with its own pacing and its own limits.       |
| `totals`                                                                                                                                  | [operations.GetConnectionStatusTotals](../../models/operations/get-connection-status-totals.md)                                           | :heavy_check_mark:                                                                                                                        | Everything summed. Null when no account is connected.                                                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.GetConnectionStatusMeta](../../models/operations/get-connection-status-meta.md)                                               | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |