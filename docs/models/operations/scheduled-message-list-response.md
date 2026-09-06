# ScheduledMessageListResponse

Messages list

## Example Usage

```typescript
import { ScheduledMessageListResponse } from "bereach/models/operations";

let value: ScheduledMessageListResponse = {
  success: true,
  messages: [
    {
      id: "<id>",
      contactId: "<id>",
      message: "<value>",
      status: "scheduled",
      scheduledSendAt: "<value>",
      sentAt: "<value>",
      campaignSlug: "<value>",
      createdAt: "1731793762268",
    },
  ],
  total: 149047,
  limit: 282829,
  offset: 685127,
  creditsUsed: 801151,
  retryAfter: 633263,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `messages`                                                                                                                                | [operations.ScheduledMessageListMessage](../../models/operations/scheduled-message-list-message.md)[]                                     | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `total`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `limit`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `offset`                                                                                                                                  | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ScheduledMessageListMeta](../../models/operations/scheduled-message-list-meta.md)                                             | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |