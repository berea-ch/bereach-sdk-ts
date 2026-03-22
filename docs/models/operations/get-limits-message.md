# GetLimitsMessage

Limits for social engagement actions: sending messages, publishing posts, replying to comments, liking comments

## Example Usage

```typescript
import { GetLimitsMessage } from "bereach/models/operations";

let value: GetLimitsMessage = {
  daily: {
    current: 330522,
    limit: 442686,
    remaining: 567882,
  },
  weekly: {
    current: 636753,
    limit: 830346,
    remaining: 534020,
  },
  minIntervalSeconds: 472297,
  nextResetDaily: new Date("2026-08-04T10:03:00.033Z"),
  nextResetWeekly: new Date("2026-10-26T08:13:16.928Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.MessageDaily](../../models/operations/message-daily.md)                           | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC)                                                  |
| `weekly`                                                                                      | [operations.MessageWeekly](../../models/operations/message-weekly.md)                         | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset                                            |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |