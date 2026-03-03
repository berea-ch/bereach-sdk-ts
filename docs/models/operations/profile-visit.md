# ProfileVisit

Limits for visiting LinkedIn profiles and company pages

## Example Usage

```typescript
import { ProfileVisit } from "bereach/models/operations";

let value: ProfileVisit = {
  daily: {
    current: 41832,
    limit: 508530,
    remaining: 293170,
  },
  weekly: {
    current: 96344,
    limit: 944086,
    remaining: 791982,
  },
  minIntervalSeconds: 483792,
  nextResetDaily: new Date("2025-03-08T06:07:49.232Z"),
  nextResetWeekly: null,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ProfileVisitDaily](../../models/operations/profile-visit-daily.md)                | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC)                                                  |
| `weekly`                                                                                      | [operations.ProfileVisitWeekly](../../models/operations/profile-visit-weekly.md)              | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset                                            |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |