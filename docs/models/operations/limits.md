# Limits

## Example Usage

```typescript
import { Limits } from "bereach/models/operations";

let value: Limits = {
  connectionRequest: {
    uncapped: false,
    daily: {
      current: 392167,
      limit: 620172,
      remaining: 53997,
    },
    weekly: {
      current: 905903,
      limit: 617573,
      remaining: 804803,
    },
    minIntervalSeconds: 376830,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
  message: {
    uncapped: false,
    daily: {
      current: 567882,
      limit: 669069,
      remaining: 636753,
    },
    weekly: {
      current: 534020,
      limit: 472297,
      remaining: 863521,
    },
    minIntervalSeconds: 197147,
    nextResetDaily: "<value>",
    nextResetWeekly: null,
  },
  profileVisit: {
    uncapped: true,
    daily: {
      current: 293170,
      limit: 692882,
      remaining: 96344,
    },
    weekly: {
      current: 791982,
      limit: 483792,
      remaining: 394394,
    },
    minIntervalSeconds: 558979,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
  scraping: {
    uncapped: true,
    daily: {
      current: 137081,
      limit: 85944,
      remaining: 814423,
    },
    weekly: {
      current: 285349,
      limit: 899452,
      remaining: 708085,
    },
    minIntervalSeconds: 992300,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `connectionRequest`                                                                | [operations.ConnectionRequest](../../models/operations/connection-request.md)      | :heavy_check_mark:                                                                 | Limits for sending LinkedIn connection requests                                    |
| `message`                                                                          | [operations.GetLimitsMessage](../../models/operations/get-limits-message.md)       | :heavy_check_mark:                                                                 | Limits for sending DMs                                                             |
| `profileVisit`                                                                     | [operations.ProfileVisit](../../models/operations/profile-visit.md)                | :heavy_check_mark:                                                                 | Limits for visiting LinkedIn profiles and company pages                            |
| `scraping`                                                                         | [operations.Scraping](../../models/operations/scraping.md)                         | :heavy_check_mark:                                                                 | Limits for data collection: search, collecting posts/likes/comments, listing chats |
| `post`                                                                             | [operations.GetLimitsPost](../../models/operations/get-limits-post.md)             | :heavy_minus_sign:                                                                 | Limits for publishing LinkedIn posts                                               |
| `acceptInvitation`                                                                 | [operations.AcceptInvitation](../../models/operations/accept-invitation.md)        | :heavy_minus_sign:                                                                 | Limits for accepting connection invitations                                        |
| `commentPost`                                                                      | [operations.CommentPost](../../models/operations/comment-post.md)                  | :heavy_minus_sign:                                                                 | Limits for commenting on posts                                                     |
| `replyComment`                                                                     | [operations.ReplyComment](../../models/operations/reply-comment.md)                | :heavy_minus_sign:                                                                 | Limits for replying to comments                                                    |
| `profile`                                                                          | [operations.GetLimitsProfile](../../models/operations/get-limits-profile.md)       | :heavy_minus_sign:                                                                 | Limits for structured profile reads.                                               |
| `engagement`                                                                       | [operations.Engagement](../../models/operations/engagement.md)                     | :heavy_minus_sign:                                                                 | Limits for likes and reactions.                                                    |