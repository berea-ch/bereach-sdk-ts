# FindLinkedInConversationResponse

Conversation found (or not)

## Example Usage

```typescript
import { FindLinkedInConversationResponse } from "bereach/models/operations";

let value: FindLinkedInConversationResponse = {
  success: true,
  found: false,
  conversation: {
    conversationUrn: "<value>",
  },
  messages: [],
  creditsUsed: 767133,
  retryAfter: 886039,
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                              | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `found`                                                                                                                | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `conversation`                                                                                                         | [operations.FindLinkedInConversationConversation](../../models/operations/find-linked-in-conversation-conversation.md) | :heavy_check_mark:                                                                                                     | Lightweight conversation reference (O(1) lookup returns URN only, not full details).                                   |
| `messages`                                                                                                             | [operations.FindLinkedInConversationMessage](../../models/operations/find-linked-in-conversation-message.md)[]         | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `creditsUsed`                                                                                                          | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                   |
| `retryAfter`                                                                                                           | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Seconds to wait before making another call of the same type. 0 means no wait needed.                                   |