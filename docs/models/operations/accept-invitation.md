# AcceptInvitation

Limits for accepting connection invitations

## Example Usage

```typescript
import { AcceptInvitation } from "bereach/models/operations";

let value: AcceptInvitation = {
  daily: {
    current: 745035,
    limit: 967977,
    remaining: 920838,
  },
  weekly: {
    current: 676755,
    limit: 33965,
    remaining: 762167,
  },
  minIntervalSeconds: 598595,
  nextResetDaily: new Date("2024-10-28T13:42:49.201Z"),
  nextResetWeekly: new Date("2026-05-06T07:00:14.838Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.AcceptInvitationDaily2](../../models/operations/accept-invitation-daily2.md)      | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.AcceptInvitationWeekly2](../../models/operations/accept-invitation-weekly2.md)    | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |