# FindLinkedInConversationResponse

Conversation found (or not)

## Example Usage

```typescript
import { FindLinkedInConversationResponse } from "bereach/models/operations";

let value: FindLinkedInConversationResponse = {
  success: true,
  found: true,
  conversation: {
    conversationUrn: "<value>",
  },
  messages: [],
  creditsUsed: 26553,
  retryAfter: 767133,
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                              | *true*                                                                                                                 | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `found`                                                                                                                | *boolean*                                                                                                              | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `conversation`                                                                                                         | [operations.FindLinkedInConversationConversation](../../models/operations/find-linked-in-conversation-conversation.md) | :heavy_check_mark:                                                                                                     | Lightweight conversation reference (O(1) lookup returns URN only, not full details).                                   |
| `messages`                                                                                                             | [operations.FindLinkedInConversationMessage](../../models/operations/find-linked-in-conversation-message.md)[]         | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `creditsUsed`                                                                                                          | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                                   |
| `retryAfter`                                                                                                           | *number*                                                                                                               | :heavy_check_mark:                                                                                                     | Seconds to wait before making another call of the same type. 0 means no wait needed.                                   |