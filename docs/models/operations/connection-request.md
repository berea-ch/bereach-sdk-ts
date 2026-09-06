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
  nextResetDaily: "<value>",
  nextResetWeekly: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `daily`                                                                                     | [operations.ConnectionRequestDaily](../../models/operations/connection-request-daily.md)    | :heavy_check_mark:                                                                          | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.  |
| `weekly`                                                                                    | [operations.ConnectionRequestWeekly](../../models/operations/connection-request-weekly.md)  | :heavy_check_mark:                                                                          | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type. |
| `minIntervalSeconds`                                                                        | *number*                                                                                    | :heavy_check_mark:                                                                          | Minimum delay in seconds required between two consecutive actions of this type              |
| `nextResetDaily`                                                                            | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                 |
| `nextResetWeekly`                                                                           | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                 |