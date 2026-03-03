# GetMyLimitsMessage

Limits for social engagement actions: sending messages, publishing posts, replying to comments, liking comments

## Example Usage

```typescript
import { GetMyLimitsMessage } from "bereach/models/operations";

let value: GetMyLimitsMessage = {
  daily: {
    current: 278613,
    limit: 537376,
    remaining: 221249,
  },
  weekly: {
    current: 252572,
    limit: 664834,
    remaining: 626371,
  },
  minIntervalSeconds: 88226,
  nextResetDaily: new Date("2025-09-26T11:45:50.455Z"),
  nextResetWeekly: new Date("2026-02-12T10:23:30.292Z"),
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