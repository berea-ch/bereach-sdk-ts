# Limits

## Example Usage

```typescript
import { Limits } from "bereach/models/operations";

let value: Limits = {
  connectionRequest: {
    daily: {
      current: 343739,
      limit: 632124,
      remaining: 392167,
    },
    weekly: {
      current: 53997,
      limit: 183170,
      remaining: 905903,
    },
    minIntervalSeconds: 407168,
    nextResetDaily: new Date("2025-01-28T12:20:37.701Z"),
    nextResetWeekly: new Date("2026-06-21T23:56:45.599Z"),
  },
  message: {
    daily: {
      current: 330522,
      limit: 442686,
      remaining: 567882,
    },
    weekly: {
      current: 636753,
      limit: 830346,
      remaining: 534020,
    },
    minIntervalSeconds: 748795,
    nextResetDaily: new Date("2026-11-25T05:18:15.375Z"),
    nextResetWeekly: new Date("2024-08-04T01:46:21.568Z"),
  },
  profileVisit: {
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
    minIntervalSeconds: 15601,
    nextResetDaily: new Date("2025-03-20T20:21:59.635Z"),
    nextResetWeekly: new Date("2024-11-28T05:15:02.669Z"),
  },
  scraping: {
    daily: {
      current: 761224,
      limit: 601148,
      remaining: 137081,
    },
    weekly: {
      current: 407027,
      limit: 410694,
      remaining: 195167,
    },
    minIntervalSeconds: 586077,
    nextResetDaily: new Date("2026-11-15T20:01:53.215Z"),
    nextResetWeekly: new Date("2026-12-14T23:31:15.376Z"),
  },
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `connectionRequest`                                                                                             | [operations.ConnectionRequest](../../models/operations/connection-request.md)                                   | :heavy_check_mark:                                                                                              | Limits for sending LinkedIn connection requests                                                                 |
| `message`                                                                                                       | [operations.GetLimitsMessage](../../models/operations/get-limits-message.md)                                    | :heavy_check_mark:                                                                                              | Limits for social engagement actions: sending messages, publishing posts, replying to comments, liking comments |
| `profileVisit`                                                                                                  | [operations.ProfileVisit](../../models/operations/profile-visit.md)                                             | :heavy_check_mark:                                                                                              | Limits for visiting LinkedIn profiles and company pages                                                         |
| `scraping`                                                                                                      | [operations.Scraping](../../models/operations/scraping.md)                                                      | :heavy_check_mark:                                                                                              | Limits for data collection: search, collecting posts/likes/comments, fetching followers, listing chats          |