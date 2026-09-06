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
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
  },
  message: {
    daily: {
      current: 442686,
      limit: 567882,
      remaining: 669069,
    },
    weekly: {
      current: 830346,
      limit: 534020,
      remaining: 472297,
    },
    minIntervalSeconds: 488543,
    nextResetDaily: null,
    nextResetWeekly: "<value>",
  },
  profileVisit: {
    daily: {
      current: 303119,
      limit: 558979,
      remaining: 407027,
    },
    weekly: {
      current: 293170,
      limit: 692882,
      remaining: 96344,
    },
    minIntervalSeconds: 195167,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
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
    minIntervalSeconds: 474427,
    nextResetDaily: "<value>",
    nextResetWeekly: "<value>",
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
| `profile`                                                                                              | [operations.GetLimitsProfile](../../models/operations/get-limits-profile.md)                           | :heavy_minus_sign:                                                                                     | Limits for structured profile reads.                                                                   |
| `engagement`                                                                                           | [operations.Engagement](../../models/operations/engagement.md)                                         | :heavy_minus_sign:                                                                                     | Limits for likes and reactions.                                                                        |