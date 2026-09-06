# CommentPost

Limits for commenting on posts

## Example Usage

```typescript
import { CommentPost } from "bereach/models/operations";

let value: CommentPost = {
  daily: {
    current: 48144,
    limit: 410434,
    remaining: 64171,
  },
  weekly: {
    current: 547416,
    limit: 782349,
    remaining: 611258,
  },
  minIntervalSeconds: 241116,
  nextResetDaily: "<value>",
  nextResetWeekly: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `daily`                                                                                     | [operations.CommentPostDaily](../../models/operations/comment-post-daily.md)                | :heavy_check_mark:                                                                          | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.  |
| `weekly`                                                                                    | [operations.CommentPostWeekly](../../models/operations/comment-post-weekly.md)              | :heavy_check_mark:                                                                          | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type. |
| `minIntervalSeconds`                                                                        | *number*                                                                                    | :heavy_check_mark:                                                                          | Minimum delay in seconds required between two consecutive actions of this type              |
| `nextResetDaily`                                                                            | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                 |
| `nextResetWeekly`                                                                           | *string*                                                                                    | :heavy_check_mark:                                                                          | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                 |