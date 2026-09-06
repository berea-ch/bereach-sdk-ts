# ReplyComment

Limits for replying to comments

## Example Usage

```typescript
import { ReplyComment } from "bereach/models/operations";

let value: ReplyComment = {
  daily: {
    current: 67712,
    limit: 870988,
    remaining: 752517,
  },
  weekly: {
    current: 846312,
    limit: 796048,
    remaining: 666911,
  },
  minIntervalSeconds: 547645,
  nextResetDaily: "<value>",
  nextResetWeekly: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `daily`                                                                                     | [operations.ReplyCommentDaily](../../models/operations/reply-comment-daily.md)              | :heavy_check_mark:                                                                          | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.  |
| `weekly`                                                                                    | [operations.ReplyCommentWeekly](../../models/operations/reply-comment-weekly.md)            | :heavy_check_mark:                                                                          | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type. |
| `minIntervalSeconds`                                                                        | *number*                                                                                    | :heavy_check_mark:                                                                          | Minimum delay in seconds required between two consecutive actions of this type              |
| `nextResetDaily`                                                                            | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                 |
| `nextResetWeekly`                                                                           | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                 |