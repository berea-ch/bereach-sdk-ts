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
  nextResetDaily: new Date("2026-10-26T08:13:16.928Z"),
  nextResetWeekly: new Date("2026-11-04T07:49:09.645Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.MessageDaily](../../models/operations/message-daily.md)                           | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.MessageWeekly](../../models/operations/message-weekly.md)                         | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |