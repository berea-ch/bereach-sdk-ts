# Limits

## Example Usage

```typescript
import { Limits } from "bereach/models/operations";

let value: Limits = {
  connectionRequest: {
    daily: {
      current: 632124,
      limit: 392167,
      remaining: 620172,
    },
    weekly: {
      current: 359046,
      limit: 376830,
      remaining: 823903,
    },
    minIntervalSeconds: 332064,
    nextResetDaily: new Date("2026-11-25T05:18:15.375Z"),
    nextResetWeekly: new Date("2024-08-04T01:46:21.568Z"),
  },
  message: {
    daily: {
      current: 442686,
      limit: 567882,
      remaining: 669069,
    },
    weekly: null,
    minIntervalSeconds: 405884,
    nextResetDaily: new Date("2024-11-28T05:15:02.669Z"),
    nextResetWeekly: new Date("2025-03-22T02:27:07.575Z"),
  },
  profileVisit: {
    daily: {
      current: 195167,
      limit: 586077,
      remaining: 957879,
    },
    weekly: {
      current: 293170,
      limit: 692882,
      remaining: 96344,
    },
    minIntervalSeconds: 984471,
    nextResetDaily: new Date("2024-09-08T18:18:38.386Z"),
    nextResetWeekly: new Date("2024-06-30T16:38:20.025Z"),
  },
  scraping: {
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
    minIntervalSeconds: 715944,
    nextResetDaily: new Date("2024-06-15T02:49:32.724Z"),
    nextResetWeekly: new Date("2026-02-12T12:54:07.747Z"),
  },
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `connectionRequest`                                                                                    | [operations.ConnectionRequest](../../models/operations/connection-request.md)                          | :heavy_check_mark:                                                                                     | Limits for sending LinkedIn connection requests                                                        |
| `message`                                                                                              | [operations.GetLimitsMessage](../../models/operations/get-limits-message.md)                           | :heavy_check_mark:                                                                                     | Limits for sending DMs                                                                                 |
| `profileVisit`                                                                                         | [operations.ProfileVisit](../../models/operations/profile-visit.md)                                    | :heavy_check_mark:                                                                                     | Limits for visiting LinkedIn profiles and company pages                                                |
| `scraping`                                                                                             | [operations.Scraping](../../models/operations/scraping.md)                                             | :heavy_check_mark:                                                                                     | Limits for data collection: search, collecting posts/likes/comments, fetching followers, listing chats |
| `post`                                                                                                 | [operations.GetLimitsPost](../../models/operations/get-limits-post.md)                                 | :heavy_minus_sign:                                                                                     | Limits for publishing LinkedIn posts                                                                   |
| `acceptInvitation`                                                                                     | [operations.AcceptInvitation](../../models/operations/accept-invitation.md)                            | :heavy_minus_sign:                                                                                     | Limits for accepting connection invitations                                                            |
| `commentPost`                                                                                          | [operations.CommentPost](../../models/operations/comment-post.md)                                      | :heavy_minus_sign:                                                                                     | Limits for commenting on posts                                                                         |
| `replyComment`                                                                                         | [operations.ReplyComment](../../models/operations/reply-comment.md)                                    | :heavy_minus_sign:                                                                                     | Limits for replying to comments                                                                        |
| `chatSearch`                                                                                           | [operations.ChatSearch](../../models/operations/chat-search.md)                                        | :heavy_minus_sign:                                                                                     | Limits for searching chat conversations                                                                |