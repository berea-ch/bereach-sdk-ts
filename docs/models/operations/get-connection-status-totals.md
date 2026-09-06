# GetConnectionStatusTotals

Everything summed. Null when no account is connected.

## Example Usage

```typescript
import { GetConnectionStatusTotals } from "bereach/models/operations";

let value: GetConnectionStatusTotals = {
  waitingTotal: 963362,
  awaitingResponse: 108239,
  sentLast24h: 612138,
  acceptedLast24h: 775473,
  expectedNext24h: null,
  expectedIsPartial: false,
  oldestWaitingHours: 38367,
  accountsSending: 717717,
  accountsBlocked: 355703,
  accountsUnreadable: 444087,
  next: null,
};
```

## Fields

| Field                                                                                                                               | Type                                                                                                                                | Required                                                                                                                            | Description                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `waitingTotal`                                                                                                                      | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `awaitingResponse`                                                                                                                  | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `sentLast24h`                                                                                                                       | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `acceptedLast24h`                                                                                                                   | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `expectedNext24h`                                                                                                                   | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `expectedIsPartial`                                                                                                                 | *boolean*                                                                                                                           | :heavy_check_mark:                                                                                                                  | True when some accounts could not be estimated, so the expected figure is a floor rather than a total.                              |
| `oldestWaitingHours`                                                                                                                | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `accountsSending`                                                                                                                   | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `accountsBlocked`                                                                                                                   | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `accountsUnreadable`                                                                                                                | *number*                                                                                                                            | :heavy_check_mark:                                                                                                                  | N/A                                                                                                                                 |
| `next`                                                                                                                              | [operations.Next](../../models/operations/next.md)                                                                                  | :heavy_check_mark:                                                                                                                  | Who goes next overall, named only when exactly one account is sending. With several sending at once there is no single next person. |