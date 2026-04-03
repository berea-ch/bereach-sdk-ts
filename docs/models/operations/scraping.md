# Scraping

Limits for data collection: search, collecting posts/likes/comments, fetching followers, listing chats

## Example Usage

```typescript
import { Scraping } from "bereach/models/operations";

let value: Scraping = {
  daily: {
    current: 601148,
    limit: 137081,
    remaining: 85944,
  },
  weekly: {
    current: 890676,
    limit: 285349,
    remaining: 899452,
  },
  minIntervalSeconds: 708085,
  nextResetDaily: new Date("2025-09-13T20:14:45.279Z"),
  nextResetWeekly: null,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ScrapingDaily](../../models/operations/scraping-daily.md)                         | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC). Null if not configured for this action type.    |
| `weekly`                                                                                      | [operations.ScrapingWeekly](../../models/operations/scraping-weekly.md)                       | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset. Null if not configured.                   |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |