# FindConversationResponse

Conversation found (or not)

## Example Usage

```typescript
import { FindConversationResponse } from "bereach/models/operations";

let value: FindConversationResponse = {
  success: true,
  found: false,
  conversation: {
    conversationUrn: "<value>",
  },
  messages: null,
  creditsUsed: 264766,
  retryAfter: 856891,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `success`                                                                                            | *true*                                                                                               | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `found`                                                                                              | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `conversation`                                                                                       | [operations.FindConversationConversation](../../models/operations/find-conversation-conversation.md) | :heavy_check_mark:                                                                                   | Lightweight conversation reference (O(1) lookup returns URN only, not full details).                 |
| `messages`                                                                                           | [operations.FindConversationMessage](../../models/operations/find-conversation-message.md)[]         | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `creditsUsed`                                                                                        | *number*                                                                                             | :heavy_check_mark:                                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                 |
| `retryAfter`                                                                                         | *number*                                                                                             | :heavy_check_mark:                                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed.                 |