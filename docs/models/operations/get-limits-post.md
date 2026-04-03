# GetLimitsPost

Limits for publishing LinkedIn posts

## Example Usage

```typescript
import { GetLimitsPost } from "bereach/models/operations";

let value: GetLimitsPost = {
  daily: {
    current: 601616,
    limit: 338376,
    remaining: 651787,
  },
  weekly: {
    current: 623277,
    limit: 194414,
    remaining: 997584,
  },
  minIntervalSeconds: 518838,
  nextResetDaily: null,
  nextResetWeekly: new Date("2024-03-07T02:21:37.997Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.PostDaily](../../models/operations/post-daily.md)                                 | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.PostWeekly](../../models/operations/post-weekly.md)                               | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |