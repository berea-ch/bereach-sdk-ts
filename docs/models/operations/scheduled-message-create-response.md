# ScheduledMessageCreateResponse

Message created, or an existing one returned instead

## Example Usage

```typescript
import { ScheduledMessageCreateResponse } from "bereach/models/operations";

let value: ScheduledMessageCreateResponse = {
  success: true,
  scheduledMessage: {
    id: "<id>",
    contactId: "<id>",
    message: "<value>",
    status: "draft",
    scheduledSendAt: "<value>",
    sentAt: "<value>",
    campaignSlug: "<value>",
    createdAt: "1723722288076",
  },
  creditsUsed: 993525,
  retryAfter: 629062,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `scheduledMessage`                                                                                                                        | [operations.ScheduledMessage](../../models/operations/scheduled-message.md)                                                               | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `contactName`                                                                                                                             | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | N/A                                                                                                                                       |
| `duplicate`                                                                                                                               | *boolean*                                                                                                                                 | :heavy_minus_sign:                                                                                                                        | True when an existing message was returned rather than a new one created.                                                                 |
| `cooldown`                                                                                                                                | *boolean*                                                                                                                                 | :heavy_minus_sign:                                                                                                                        | True when a recent message to this contact is holding a new one back.                                                                     |
| `cooldownReason`                                                                                                                          | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | Why the cooldown applies.                                                                                                                 |
| `campaignNote`                                                                                                                            | *string*                                                                                                                                  | :heavy_minus_sign:                                                                                                                        | Present when the requested list matched nothing and the draft was filed with the person instead; names where it landed.                   |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.ScheduledMessageCreateMeta](../../models/operations/scheduled-message-create-meta.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |