# ChatSearch

Limits for searching chat conversations

## Example Usage

```typescript
import { ChatSearch } from "bereach/models/operations";

let value: ChatSearch = {
  daily: {
    current: 960454,
    limit: 115914,
    remaining: 463627,
  },
  weekly: null,
  minIntervalSeconds: 34056,
  nextResetDaily: new Date("2024-10-15T17:47:52.904Z"),
  nextResetWeekly: null,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ChatSearchDaily](../../models/operations/chat-search-daily.md)                    | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.ChatSearchWeekly](../../models/operations/chat-search-weekly.md)                  | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |