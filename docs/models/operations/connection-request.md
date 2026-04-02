# ConnectionRequest

Limits for sending LinkedIn connection requests

## Example Usage

```typescript
import { ConnectionRequest } from "bereach/models/operations";

let value: ConnectionRequest = {
  daily: {
    current: 632124,
    limit: 392167,
    remaining: 620172,
  },
  weekly: null,
  minIntervalSeconds: 183170,
  nextResetDaily: new Date("2025-11-07T20:37:27.290Z"),
  nextResetWeekly: new Date("2026-04-07T11:45:49.375Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ConnectionRequestDaily](../../models/operations/connection-request-daily.md)      | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.ConnectionRequestWeekly](../../models/operations/connection-request-weekly.md)    | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |