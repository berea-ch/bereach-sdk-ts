# Scraping

Limits for data collection: search, collecting posts/likes/comments, fetching followers, listing chats

## Example Usage

```typescript
import { Scraping } from "bereach/models/operations";

let value: Scraping = {
  daily: {
    current: 761224,
    limit: 601148,
    remaining: 137081,
  },
  weekly: null,
  minIntervalSeconds: 814423,
  nextResetDaily: new Date("2026-09-03T04:19:37.360Z"),
  nextResetWeekly: new Date("2026-09-12T19:09:56.251Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `daily`                                                                                       | [operations.ScrapingDaily](../../models/operations/scraping-daily.md)                         | :heavy_check_mark:                                                                            | Daily usage counter (resets at midnight UTC)                                                  |
| `weekly`                                                                                      | [operations.ScrapingWeekly](../../models/operations/scraping-weekly.md)                       | :heavy_check_mark:                                                                            | Weekly usage counter (resets Monday 00:00 UTC). Null if no weekly cap for this action type.   |
| `minIntervalSeconds`                                                                          | *number*                                                                                      | :heavy_check_mark:                                                                            | Minimum delay in seconds required between two consecutive actions of this type                |
| `nextResetDaily`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next daily counter reset                                            |
| `nextResetWeekly`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | ISO 8601 timestamp of the next weekly counter reset. Null if no weekly cap.                   |