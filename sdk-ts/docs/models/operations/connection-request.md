# ConnectionRequest

Limits for sending LinkedIn connection requests

## Example Usage

```typescript
import { ConnectionRequest } from "bereach/models/operations";

let value: ConnectionRequest = {
  daily: {
    current: 343739,
    limit: 632124,
    remaining: 392167,
  },
  weekly: {
    current: 53997,
    limit: 183170,
    remaining: 905903,
  },
  minIntervalSeconds: 617573,
  nextResetDaily: new Date("2026-06-01T01:32:02.902Z"),
  nextResetWeekly: new Date("2024-12-15T04:27:46.989Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ConnectionRequestDaily](../../models/operations/connection-request-daily.md)      | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC)                                                  |
| `weekly`                                                                                      | [operations.ConnectionRequestWeekly](../../models/operations/connection-request-weekly.md)    | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset                                            |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |