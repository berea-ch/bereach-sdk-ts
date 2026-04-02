# ProfileVisit

Limits for visiting LinkedIn profiles and company pages

## Example Usage

```typescript
import { ProfileVisit } from "bereach/models/operations";

let value: ProfileVisit = {
  daily: null,
  weekly: {
    current: 293170,
    limit: 692882,
    remaining: 96344,
  },
  minIntervalSeconds: 944086,
  nextResetDaily: new Date("2025-06-14T05:40:33.290Z"),
  nextResetWeekly: new Date("2024-01-05T09:29:21.354Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ProfileVisitDaily](../../models/operations/profile-visit-daily.md)                | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.ProfileVisitWeekly](../../models/operations/profile-visit-weekly.md)              | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |