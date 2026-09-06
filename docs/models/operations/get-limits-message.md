# GetLimitsMessage

Limits for sending DMs

## Example Usage

```typescript
import { GetLimitsMessage } from "bereach/models/operations";

let value: GetLimitsMessage = {
  daily: {
    current: 442686,
    limit: 567882,
    remaining: 669069,
  },
  weekly: {
    current: 830346,
    limit: 534020,
    remaining: 472297,
  },
  minIntervalSeconds: 863521,
  nextResetDaily: "<value>",
  nextResetWeekly: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `daily`                                                                                     | [operations.MessageDaily](../../models/operations/message-daily.md)                         | :heavy_check_mark:                                                                          | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.  |
| `weekly`                                                                                    | [operations.MessageWeekly](../../models/operations/message-weekly.md)                       | :heavy_check_mark:                                                                          | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type. |
| `minIntervalSeconds`                                                                        | *number*                                                                                    | :heavy_check_mark:                                                                          | Minimum delay in seconds required between two consecutive actions of this type              |
| `nextResetDaily`                                                                            | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                 |
| `nextResetWeekly`                                                                           | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                 |